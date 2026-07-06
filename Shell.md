# Shell命令笔记
## 概述
* 使用`Ctrl+Alt+T`唤醒终端，或在应用程序中搜索`Terminal`以运行（Linux）
* 在Linux上打开Terminal，通常使用的是`bash`命令
* 类似的命令提示符式功能在`Windows`中也有所体现，如`Win+R`所运行的`cmd`程序
* 打开Linux终端界面时，一般会显示如下内容
```shell
yus@yus:~$
```
其中`@前`的字符为当前登录的用户，`@后`的字符为当前计算机名称，`~`是当前工作目录（/home）的缩写，即`/home/yus`，`$`代表你不是root用户

## 最常见的命令
* cd 切换目录  
绝对路径：/bin/bash/  
相对路径：`.`（当前目录）/`..`（父目录）  
`-`切换上个目录
* pwd 打印路径
* cp 复制
* mv 剪切  
亦用作**重命名**工具
* rm 删除
* man 教程
* apt 软件包管理器
* echo 回显
* ls 列出文件  
  `-l` 以列表模式显示文件属性
    ```shell
    drwx------ 4 yus  yus  4096  7月  5 11:47 snap
    -rwxr-xr-x 1 root root   54  7月  5 11:49 SwitchShell.sh
    # 读写运行权限 硬连接数 所有者 所属组 大小 时间 文件名 
    ```
  `-a` （all）列出所有文件（包括隐藏文件）

* test `[` 检验文件存在性

## 与单文件有关的r/w命令
* cat 打印文件内容
```shell
cat 1.txt
```
* sort 排序文件内容  
将文件各行按照字典排序后再输出
```shell
sort 1.txt
```
* uniq 去重  
去掉文件中连续重复的行
```shell
uniq 1.txt
```
* grep 查找  
在指定文件中查找所有符合参数的行  
要求书写**正则表达式**
```shell
grep
```
* find 查找  
递归地查找满足查找条件的文件  
不涉及`grep`对于内容的查找，仅查找文件名/文件类型/修改日期等  
`fd`相较于`find`更加人性化  
例：在下载目录查找所有超过30天的ZIP文件  
```shell
find ~/Downloads -type f -name "*.zip" -mtime +30
```

* sed 替换
```shell
sed -i 's/要修改的内容/修改后的内容/g' 1.txt
```
其中`-i`表示直接修改文件，`s/`（substitute）是替换的指令，`/`用来分隔匹配字符与替换内容，`/g`（global）表示在**每一行中**替换所有匹配项

* awk 提取   
最常见的用途是处理有规则格式的数据文件（比如 CSV）

* head / tail 读取头部 / 尾部内容  
针对长文件  
`--lines=1`读取文件前 / 后1行内容并输出

* less 读取全文  
特点是可以在终端中以键盘控制方向以**滚动读取**  
退出按`q`

* file 输出属性

## 文本编辑器
* nano
* vim/vi  
默认进入**浏览模式**，按`i`键进入**编辑模式**  
按`esc`退出编辑模式，输入`:q`退出，输入`:q!`**强制**退出

## 系统级命令
* systemctl
* ss

## 远程shell
1. 配置远程ssh服务
```shell
sudo apt install openssh-server
sudo systemctl enable ssh && sudo systemctl start ssh
ssh-keygen #生成在/home/$USER中 还需要在本地运行下一行代码
ssh-copyid user@hostname
```

2. 以Xshell为例连接远程ssh  
需要注意的是，在远程主机中生成公钥后只需运行`ssh-copyid`即可，**无需也不能**将公钥*导入Xshell*

<img src="https://pub-7e5b8ad9a5864c57932040aa1e7b0318.r2.dev/ssh-1.png" width=500 alt="SSH图1">
<img src="https://pub-7e5b8ad9a5864c57932040aa1e7b0318.r2.dev/ssh-2.png" width=400 alt="SSH图2">  

2. ssh服务常见语法  
    * 在本地终端中连接远程服务器  
    `-p`指定端口  
    `-i`使用密钥（推荐）  

例如：
```shell
ssh user@hostname
ssh -i /.../id_rsa user@hostname
```

3. 利用`rsync`或`scp`与远程主机互传文件  
`rsync`适用于**大文件**传输，`scp`适用于**小文件*  
    ```shell
    scp ~/1.txt user@hostname:~/
    rsync -avz ~/1.txt user@hostname:~/
    ```  


    * rsync语法  
    `-a`  保留属性复制（归档模式）  
    `-v` 可视化输出  
    `-z`  传输时压缩（远程推荐）  
    `--partial`  启用断点续传  
    `--progress`  显示进度


## 通用语法
### 输入输出
* `&&`  
用来连接两个命令。只有当前面的命令执行成功（返回状态码为 0）时，才会继续执行后面的命令。如果前面的命令失败了，后面的命令就直接被跳过。
```shell
sudo apt update && sudo apt install openssh-server
```
* `|` 管道Pipe  
把前一个命令的输出结果，变成后一个命令的输入
```shell
cat output.txt | grep "Hello"
# cat 读取文件内容，通过管道传给 grep，grep 在其中筛选出包含 "Hello" 的行
```

* `>` 覆盖重定向  
将前一命令的输出内容写入到一个文件中，会新建文件/覆盖原文件内容
* `>>` 追加重定向  
将前一命令的输出内容写入到一个文件中，**不会覆盖原文件**内容，适合输出log日志
```shell
date >> date.txt
```

* `<` 输入重定向  
改变命令的输入源，从文件读取命令而非从键盘读取
```shell
cat < date.txt
```

### 条件、循环语句
* if 条件  
```shell
if [ 条件判断式 ]; then
    # 当条件满足（返回0）时执行
elif [ 另一个条件判断式 ]; then
    # 当上一个条件不满足，且本条件满足时执行
else
    # 所有条件都不满足时执行
fi 
```
下方代码的分号代替了回车键，常用作终端中的命令执行。  
回车键与换行符`;`均表示命令结束，所以上下两个代码的语法均**正确**。  
但复杂的shell脚本建议换行写作
```shell
if []; then []; fi
```
* while 无限循环
```shell
while [ 条件判断式 ]
do
    # 只要条件成立（返回0），就一直执行
done
```
* for 有限循环
```shell
for 变量名 in 取值列表（值1，值2，值3） ...
do
    # 遍历执行循环
done
```

### 定义变量  
使用变量时要加入`$`
```shell
h="hello"
echo $h
```
以上程序运行后会输出`hello`
## 键盘功能
* `Tab` 自动补全
* `↑ / ↓` 按照输入顺序切换命令

## 解释器指示行 *Shebang*
在可执行的shell文件中，文件以下方代码开头
```shell
#!/bin/bash
```
意思是把脚本内容交给`/bin/bash`程序去执行
### set命令参数
* `-e`遇错即停止  
只要任何一行代码执行失败，则退出程序
* `-u` 禁用未定义变量  
如果使用一个**未赋值**的变量，则退出程序
* `-x` 调试模式  
把脚本执行的每一步命令、变量替换后的真实样子，全部打印
* `-o pipefail` *管道错误透传*  
只要管道（│）里的任何一个命令失败，整个管道就判定为失败
### shell的严格模式
```shell
#!/bin/bash
set -eux -o pipefall
```

## 正则表达式
## 通配符扩展