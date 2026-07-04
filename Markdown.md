# 我的第一个MD语法笔记
<!-- 目录开始 -->
<h2>目录</h2>
<ul>
    <li>1. <a href="#1st">前言</a></li>
    <li>2. <a href="#title">标题</a></li>
    <li>3. <a href="#codes">代码区</a></li>
    <li>4. <a href="#text">文字样式</a>
    <ul>
        <li>4.1 <a href="#code">代码</a></li>
        <li>4.2 <a href="#font">常见字体</a></li>
        <li>4.3 <a href="#mark">文本高亮</a></li>
        <li>4.4 <a href="#fold">内容折叠</a></li>
    </ul>
    <li>5. <a href="#paragraph">段落分割</a>
    <li>6. <a href="#quote">引言</a>
    <li>7. <a href="#list">列表</a>
        <ul>
        <li>7.1 <a href='#fundamental-list'>基础样式</a>
        <li>7.2 <a href='#tidier-list'>设定对齐方式</a>
    <li>8. <a href="#links">超链接</a>
    <ul>
        <li>8.1 <a href="#fundamental-link">简单超链接</a></li>
        <li>8.2 <a href="#global-link">全局赋值</a></li>
    </ul>
    <li>9. <a href="#photo">插入图片</a>
    <ul>
        <li>9.1 <a href="#fundamental-photo">简单插入</a></li>
        <li>9.2 <a href="#global-photo">全局插入</a></li>
        <li>9.3 <a href="#html-photo">以html高级插入</a></li>
    </ul>
    <li>10. <a href="#todo">To-Do代办</a>
    <li>11. <a href="#formula">公式</a>
    <li>12. <a href="#menu">目录</a>
    <li>13. <a href="#last">后记</a>
<hr>
<!-- 目录结束 -->



## 前言 <a id="1st"></a>

* 这份文件是我在2022年初三网课时期无聊所作，当时太喜欢装逼导致整个文档都是英文缺乏可读性，在高三毕业后进行维护与修改

* 文档首次创作时间  
1:40 (UTC+8), 18th Dec. 2022  
纪念一下无忧的中学时代

* 原创性声明：所有内容均为个人手写、手敲。同时参考了一些B站视频，致敬。



## 标题 <a id="title"></a>

```markdown
共有六个标题，标题大小随着级数增加而减小
几个井号就是几级标题
# +内容       |   //一级标题
## +内容      |   //二级标题
### +内容     |   //三级标题
#### +内容    |   //四级标题
##### +内容   |   //五级标题
###### +内容  |   //六级标题
```

## 代码区 <a id="codes"></a>

段落代码引用
```
    ```+语言名称（可选）    
    “代码”
    ```
```   
行间代码引用
```
`“代码”`
例如很多中文中插入了一个英文代码，可以用此引用方式
```

## 文字样式 <a id="text"></a>

1. 代码  <a id="code"></a>  
    **字体加粗**
    ```
    **加粗的内容**
    ```
    删除线  ~~删除~~
    ```
    ~~被删除的文字~~
    ```
    *斜体*
    ```
    *斜体内容*
    ```
    ***又斜体又加粗***
    ```
    ***内容***
    ```
    <ins>下划线</ins>
    ```
    <ins>被划线的内容</ins>
    ```

2. 常见字体 <a id="font"></a>
（受设备和软件限制）
    |中文名|英文名|
    |:--:|:--:|
    |黑体|SimHei：`<font face='SimHei'>`|
    |宋体|SimSun：`<font face='SimSun'>`|
    |新宋体|NSimSun：`<font face='NSimSun'>`|
    |仿宋|FangSong：`<font face='FangSong'>`|
    |楷体|KaiTi：`<font face='KaiTi'>`|
    |仿宋_GB2312|FangSong_GB2312：`<font face='FangSong_GB2312'>`|
    |楷体_GB2312|KaiTi_GB2312：`<font face='KaiTi_GB2312'>`|
    |微软雅黑|Microsoft Yahei：`<font face='Microsoft YaHei'>`|
```html
<font face='KaiTi' color='' size='5'>这段话会变成楷体，非常适合用来写名人名言或者引用。</font> 
```
<font face='KaiTi' size='5'>这段话会变成楷体，非常适合用来写名人名言或者引用。</font>  

3. <mark>文本高亮</mark> <a id="mark"></a>
```html
这是 <mark>重点高亮</mark> 的文字。
```

4. 内容折叠 <a id="fold"></a>
```html
<details>
<summary><b>点击展开代码解析</b></summary>
这里可以写长篇的逻辑推导、源码或者解析，默认是折叠的。
</details>
```
<details>
<summary><b>点我展开</b></summary>
APTAPTAPTAPTAPT
</details>

## 段落分割 <a id="paragraph"></a>


段落分割线
```
***
---
___
```
无序列表（黑点）
```
* contents
+ contents
- contents
```
有序列表（数字）
```
1. 自行安排序号
    1. contents
    2. contents
    3. contents
2. 自动安排序号
    0. contents
    0. contents
    0. contents
3. 让序列以给定数字开头
    X. contents
    1. contents
    2. contents
```

## 引言 <a id="quote"></a>

>"你已经是一个成熟的引用了，要学会自己引用，"   ——渥斯基硕得

```markdown
>+ 内容
```

## 列表 <a id="list"></a>

1. 基础样式 <a id="fundamental-form"></a>

    ```md
    |A1|B1|
    |----|----|
    |(1,1)|(1,2)|
    |(2,1)|(2,2)|
    ```
    |A1|B1|
    |----|----|
    |(1,1)|(1,2)|
    |(2,1)|(2,2)|

2. 设定对齐方式 <a id="tidier-form"></a>

    ```md
    |左对齐|居中对齐|右对齐|
    |:--|:--:|--:|
    |1|张三|17岁|
    |2|李四|18岁|
    |3|王五|19岁|
    ```

    |左对齐|居中对齐|右对齐|
    |:--|:--:|--:|
    |1|张三|17岁|
    |2|李四|18岁|
    |3|王五|19岁|

## 超链接 <a id="links"></a>

1. 简单超链接 <a id="fundamental-link"></a>

    ```md
    [网站名称](网址)
    ```

    [eg：baidu](https://baidu.com)

2. 全局赋值 <a id="global-link"></a>

    ```md
    [url_name][url]
    [url]=*.com
    相当于为[url]手动赋值
    ```

## 插入照片 <a id="photo"></a>

1. 简单插入 <a id="fundamental-photo"></a>

    ```md
    ![image_name](image_url/loacl path)
    ```
    For example：
        ![修沟](https://img1.baidu.com/it/u=4007079237,1123477514&fm=253&app=138&size=w931&n=0&f=JPEG&fmt=auto?sec=1671469200&t=6ef33f4ff3a8d7cf8932fc555b9b82ff)

2. 全局插入 <a id="global-photo"></a>

    ```md
    ![img_name][img1]
    ![img_name][img2]

    [img1]:*.com 
    [img2]:*.com 
    还是赋值
    ```

    For Example

    ![city1][img1]
    ![city2][img2]

    [img1]:https://t7.baidu.com/it/u=1595072465,3644073269&fm=193&f=GIF
    [img2]:https://t7.baidu.com/it/u=2397542458,3133539061&fm=193&f=GIF

3. 以html高级插入 <a id="html-photo"></a>
```html
<img src="图片链接" width="50%" align="center" alt="描述">
```

## To-Do代办 <a id="todo"></a>

```md
- [] 任务1
    - [x] 任务1.1
- [x] 任务2
- [x] 任务3

x表示已完成，无√一说
```
- [ ] 任务1
    - [x] 任务1.1
- [x] 任务2
- [x] 任务3



## 公式 <a id="formula"></a>
例：$$ f(x) = w^T x + b $$
语法：
```latex
$ y=kx+b $
用美元符号包围公式前后
```

| 上标 | 下标 | 分式 | 根式 |
| ---- | ---- | ---- | ---- |
| ^ | _ | \frac{分子}{分母} | \sqrt[次数]{内容} |



## 目录 <a id="menu"></a>
```html
<h2>目录索引</h2>
<ul>
    <li>1. <a href="#XXX">XXX</a></li>
        以上为一级标题的单行代码
        以下为二级标题的三行代码，注意缩进
        <ul>
            <li>4.1 <a href="#XXX-1">XXX-1</a></li>
        </ul>
    </li> 
</ul>
<hr>
```
* a href='' 单引号中必须加`#`，否则无法跳转
* a href='' 单引号中的东西怎么来的？
    <details>
        <summary><b>揭晓答案</b></summary>
        在对应的标题（如## ...）后加入

        ```
        <a id=""></a>
        ```
    单引号中内容自行指定
    </details>


## 后记 <a id="last"></a>
*  This file had been stored in my disk for 4 years, until I found it and uploaded it.
* last edition: **1:37 (UTC+8), 5th July, 2026.** 