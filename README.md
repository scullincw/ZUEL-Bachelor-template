# ZUEL-Bachelor-template

中南财经政法大学本科学位论文或学年论文模板，改自武汉大学本科学位论文模板。

1. 适用 TeX Live 2015 软件环境. 安装 TeX Live 2015 之后需要立即更新.  
    TeX Live 安装及更新方法，参见：http://aff.whu.edu.cn/huangzh/
2. 使用 XeLaTeX 编译.
3. 主文档是 Bachelor-template.tex .
4. 图片请放在 figures 文件夹.
5. includefile 存放的是英文封面、中英文摘要、致谢等等正文以外的部分。
    请直接在这些文件中填写相关内容,不要改变文件的位置.
6. 更多使用说明请参看 Bachelor-template-BACK.pdf , 以及源文件 Bachelor-template.tex 里的注释说明.
7. 模板下载更新地址:
    http://aff.whu.edu.cn/huangzh/



具体使用步骤
------------

**Step 1**

进入 includefile 文件夹, 打开 `frontmatter.tex`, `backmatter.tex`这两个文档, 分别填写 (1) 中文摘要、英文摘要, (2) 致谢.

**Step 2**

打开主文档 `Bachelor-template.tex`, 填写题目、作者等等信息, 书写正文.

Step 3

使用 XeLaTeX 编译. 

在`Bachelor-template.tex`的目录下，运行

```cmd
xelatex Bachelor-template.tex
```

编译的方法 {#sec-compile}
----------

默认使用 XeLaTeX 编译, 直接生成 pdf 文件.

若另存为新文档, 请确保文档保存类型为 `UTF-8`.
当然目前很多编辑器默认文字编码为 UTF-8. WinEdt 9.0
之后的版本都是默认保存为 UTF-8 的.

文档类型选择
------------

文档类型有 2 种情形:

----------------------------------------- ----------------
  `\documentclass{ZUELBachelor}`             毕业论文
  `\documentclass[forprint]{ZUELBachelor}`   毕业论文打印版
----------------------------------------- ----------------

相关解释见下节.

打印的问题
----------

i)  关于文档选项 `forprint`: 交付打印时, 建议加上选项 `forprint`,
    以消除链接文字之彩色, 避免打印字迹偏淡.

ii) 打印时留意不要缩小页面或居中. 即页面放缩方式应该是"无"(Adobe Reader
    XI 是选择"实际大小"). 有可能页面放缩方式默认为"适合可打印区域",
    会导致打印为原页面大小的 $97\%$. 文字不要居中打印, 是因为考虑到装订,
    左侧的空白留得稍多一点(模板已作预留).

iii) 遗留问题: 封面需要打印部重新制作. 校内打印部通常有现成的模板.
    我们自己做的封面, 打印部不一定好用.

**问**: 生成 PDF
文件时，不能去掉目录和文章的引用彩色方框，请问怎么解决？

**答**: 方框表示超级链接, 只在电脑上看得见. 实际打印时, 是没有的. 另外,
文档类型加选项 forprint 之后, 这些框框会隐掉的.

本文档下载更新地址: <http://aff.whu.edu.cn/huangzh/>. 使用之前,
请移步查看是否有更新.

问题反馈及建议, 请联系: huangzh\@whu.edu.cn.



Readme
------

模板文件的结构, 如下表所示:

```
ZUEL-Bachelor-template/
│  Bachelor-template.tex		//主文档. 在其中填写正文. 
│  ZUELBachelor.cls				//定义文档格式的 class file. 不可删除. 
│  
├─figures						//存放图片文件
└─includefile
        backmatter.tex			//致谢.
        frontmatter.tex			//郑重声明、中英文摘要.
```

无需也不要改变、移动上述文档的位置.

如果不习惯用 `\include{ }` 的方式加入"子文档",
当然可以把它们合并在主文档, 成为一个文档.
(但是这样并不会给我们带来方便.)

利用 WinEdt 的 Project tree, 可以方便地管理这些文件:

-   点击 WinEdt 窗口的 Project Tree 按键;

-   再点击 WinEdt 窗口的 Set Main File 按键;

接下来的管理, 已经清楚地展示在跳出的窗口中了. 再去处理其他的文件时,
还要点击 WinEdt 窗口的 Remove Main File 按键.

字体调节
--------

------------- ------
  `\songti`     宋体
  `\heiti`      黑体
  `\fangsong`   仿宋
  `\kaishu`     楷书
------------- ------

字号调节
--------

字号命令: `\zihao`

-------------- ----------------
  `\zihao{0}`    初号字 English
  `\zihao{-0}`   小初号 English
  `\zihao{1} `   一号字 English
  `\zihao{-1}`   小一号 English
  `\zihao{2} `   二号字 English
  `\zihao{-2}`   小二号 English
  `\zihao{3} `   三号字 English
  `\zihao{-3}`   小三号 English
  `\zihao{4} `   四号字 English
  `\zihao{-4}`   小四号 English
  `\zihao{5} `   五号字 English
  `\zihao{-5}`   小五号 English
  `\zihao{6} `   六号字 English
  `\zihao{-6}`   小六号 English
  `\zihao{7} `   七号字 English
  `\zihao{8} `   八号字 English
-------------- ----------------

已加入的常用宏包
----------------

**cite** 参考文献引用, 得到形如 \[3-7\] 的样式.

**color,xcolor** 支持彩色.

**enumerate** 方便自由选择 enumerate 环境的编号方式. 比如

    `\begin{enumerate}[(a)]` 得到形如 (a), (b), (c) 的编号.
    `\begin{enumerate}[i)]` 得到形如 i), ii), iii) 的编号.

另外要说明的是, `itemize`, `enumerate`, `description` 这三种 list 环境, 已经调节了其间距和缩进, 以符合中文书写的习惯.


