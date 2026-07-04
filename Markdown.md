# Getting Ready in making md files!
<!-- vscode-markdown-toc -->
* 1. [Write at the fitst time](#Writeatthefitsttime)
  * 1.1. [Hi there, welcome to my md file, today I will teach you how to use primary markdown grammar to make a file](#HitherewelcometomymdfiletodayIwillteachyouhowtouseprimarymarkdowngrammartomakeafile)
  * 1.2. [This passage was first made at the 1:40 (UTC+8), 18th Dec. 2022. Respect](#Thispassagewasfirstmadeatthe1:40UTC818thDec.2022.Respect)
  * 1.3. [Bluntly, although this file was made by me, I copied the content from website:     ,respect as well](#BluntlyalthoughthisfilewasmadebymeIcopiedthecontentfromwebsite:respectaswell)
* 2. [Title](#Title)
* 3. [Code Area](#CodeArea)
* 4. [Character's Form](#CharactersForm)
* 5. [List](#List)
* 6. [Quora](#Quora)
* 7. [Form](#Form)
* 8. ["SuperLink"](#SuperLink)
* 9. [插入照片](#)
* 10. [To-Do Lists](#To-DoLists)
* 11. [Menu](#Menu)

<!-- vscode-markdown-toc-config
	numbering=true
	autoSave=true
	/vscode-markdown-toc-config -->


## Write at the fitst time

### Hi there, welcome to my md file, today I will teach you how to use primary markdown grammar to make a file

### This passage was first made at the 1:40 (UTC+8), 18th Dec. 2022. Respect

### Bluntly, although this file was made by me, I copied the content from website:     ,respect as well

---

## Title

```markdown
//共有六个标题，标题大小随着级数增加而减小
//几个井号就是几级标题
# +内容       |   //一级标题
## +内容      |   //二级标题
### +内容     |   //三级标题
#### +内容    |   //四级标题
##### +内容   |   //五级标题
###### +内容  |   //六级标题
```

## Code Area

```markdown
//段落代码引用
    ```+语言名称    //回车
    “内容”
    ```            //表示结束
//行间代码引用
    CONTENTS+ `“内容”`
```

## Character's Form

1. 代码

    ```markdown
    //字体加粗
        **加粗的内容**
    //删除线
        ~~被删除的文字~~
    //斜体
        *斜体内容*
    //又斜体又加粗
        ***内容***
    //下划线
        <ins>contents</ins>
    //常见字体

    <font face='SimHei'>【黑体】CONTENTS</font>
    <font face='SimSun'>【宋体】CONTENTS</font>
    <font face='NSimSun'>【新宋体】CONTENTS</font>
    <font face='FangSong'>【仿宋】CONTENTS</font>
    <font face='KaiTi'>【楷体】CONTENTS</font>
    <font face='FangSong_GB2312'>【仿宋_GB2312】CONTENTS</font>
    <font face='KaiTi_GB2312'>【楷体_GB2312】CONTENTS</font>
    <font face='Microsoft YaHei'>【微软雅黑】CONTENTS</font>
    ```

2. 常见字体的表格

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

## List

```markdown
//段落分割线
    ***
    ---
    ___
//无序列表（黑点）
    * +contents
    + +contents
    - +contents
//有序列表（数字）
    //自行安排序号
    1. +contents
    2. +contents
    3. +contents
    //自动安排序号
    0. +contents
    0. +contents
    0. +contents
    //让序列以“数字X开头”
    X. +contents
    1. +contents
    2. +contents
```

## Quora

>"你已经是一个成熟的引用了，要学会自己引用，"   ——渥斯基硕得

```markdown
>+contents
//Enter
```

## Form

1. Primary

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

2. 设定对齐方式

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

## "SuperLink"

1. 简单超链接

    ```md
    [网站名称](网址])
    ```

    [eg：baidu](https://baidu.com)

2. 全局声明 一

    ```md
    [url_name][url]
    [url]=*.com
    ```

3. 全局声明 二

   ```md
   [url_name][]
   [url]=*.com
   ```

## 插入照片

1. 简单插入

    ```md
    ![image_name](image_url/loacl path)
    ```

    For example：
        ![修沟](https://img1.baidu.com/it/u=4007079237,1123477514&fm=253&app=138&size=w931&n=0&f=JPEG&fmt=auto?sec=1671469200&t=6ef33f4ff3a8d7cf8932fc555b9b82ff)

2. 全局插入

    ```md
    ![img_name][img1]
    ![img_name][img2]

    [img1]:*.com 
    [img2]:*.com 
    ```

    For Example

    ![city1][img1]
    ![city2][img2]

    [img1]:https://t7.baidu.com/it/u=1595072465,3644073269&fm=193&f=GIF
    [img2]:https://t7.baidu.com/it/u=2397542458,3133539061&fm=193&f=GIF

## To-Do Lists

```md
+ [ ] Name
    + [x] Name
- [x] Name
* [x] Name
```

## Menu

* As there isn't have direct TOC modole we can use in VS code, we need to install a moudle from plugin store. It named "Markdown TOC"
* After install this moudle, put your mouse on the loction that you want to insert the menu. Type "CTRL+SHIFT+P" to ask for command board, and Type "Generate". After that, choose "Generate TOC for markdown" 
* Enjoy!

## Thanks
* As the biginning of the md files said, this markdown file was first made at the 1:40 (UTC+8), 18th Dec, 2022, which is the period I was in 9th grade
* To spend time in lockdown period, I just opened bilibili and search for the grammar of markdown language. This file had been stored in my disk for 4 years, until I found it and uploaded it.
* last edit: **22:49 (UTC+8), 4th July, 2026**. 