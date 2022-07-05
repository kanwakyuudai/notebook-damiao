# 6-27
## 二进制0-140
0
1
10
11
100
101
110
111
1000
1001
1010
1011
1100
1101
1110
1111
10000
10001
10010
10011
10100
10101
10110
10111
11000
11001
11010
11011
11100
11101
11110
11111
100000
100001
100010
100011
100100
100101
100110
100111
101000
101001
101010
101011
101100
101101
101110
101111
110000
110001
110010
110011
110100
110101
110110
110111
111000
111001
111010
111011
111100
111101
111110
111111
1000000
1000001
1000010
1000011
1000100
1000101
1000110
1000111
1001000
1001001
1001010
1001011
1001100
1001101
1001110
1001111
1010000
1010001
1010010
1010011
1010100
1010101
1010110
1010111
1011000
1011001
1011010
1011011
1011100
1011101
1011110
1011111
1100000
1100001
1100010
1100011
1100100
1100101
1100110
1100111
1101000
1101001
1101010
1101011
1101100
1101101
1101110
1101111
1110000
1110001
1110010
1110011
1110100
1110101
1110110
1110111
1111000
1111001
1111010
1111011
1111100
1111101
1111110
1111111
10000000
10000001
10000010
10000011
10000100
10000101
10000110
10000111
10001000
10001001
10001010
10001011
# 6-28
## 思考题
* 什么是ascii码表？
  * 美国标准编码表，定义了阿拉伯数字、大小写英文字母、制表符等字符。

* 计算机为什么使用二进制？
  * 非理想状态下电路中的电压在不容易精确控制，将电压区分成高低电压两种状态（0和1），对应二进制。

* 什么是数字信号，什么是模拟信号？
  * 模拟信号是连续的，容易被干扰，适合近距离通讯；数字信号是离散的。

* 编码与编号有什么区别？
  * 编码指按照一定规则转换信息对应的代码；编号指按一定顺序给事物排序。

* Unicode是编码还是编号？
  * 编号。

* bmp格式是如何保存图片的？文件内有哪些信息，以什么方式保存的？使用十六进制编辑器进行编辑验证。
  * 文件头（包含格式，图片长宽像素等信息）+每个像素的RGB实际值；以文本形式保存。

* gif格式是如何保存图片的？为什么图片放大能看到类似麻点的内容？
  * 分析图片色彩，找出最接近的256种色彩，超出的色彩将被替换为类似深浅颜色相互交替，放大之后呈现“麻点”效果。

* 几种图片格式有什么主要的区别？合适的场景分别是？
  * JPEG是有损压缩，压缩率高，适合处理自然照片；PNG是无损压缩，适合处理设备截图；WebP是有损压缩，质量更高，适合移动设备等需要节省带宽和性能的场景。

* 将748367转换为5进制。
  * 142421432
  * `748367..toString(5)`
## 讲解思考题
* 什么是ascii码表？
  * 就是对128个符号进行了编号
    * a 97
    * A 65
    * 0 48
    * 空格 32
    * 回车 10
    * 换行 13

* 计算机为什么使用二进制？
* 因为使用二进制可以消除误差

* 什么是数字信号，什么是模拟信号？
  * 数字信号即将设备中的模拟量理解成0跟1，即为数字信号
    * 数字信号是离散的
  * 模拟信号则是直接将设备中的物理量参与设备的运行及物理量的计算及转换等
    * 模拟信号一般是连续的
    * 调制解调器（Moderm, 猫）
    * 将数字信号与模拟信号进行转换的

* 编码与编号有什么区别？
  * 在计算机/编程语境下
  * 编码特指将信息（可以是编号，也可以不是编号）表示成二进制，是一个动词

* 编号就只是对事物进行编号（与进制无关）
  * 如unicode对所有的文字符号进行了编号
  * UTF-8/UTF-16则是对编号的变长编码规则
  * ascii对基本的英文标点及字母等进行了编号

* Unicode是编码还是编号？
  * 是编号
  * unicode标准本身并不涉及将编号如何存储为二进制

* bmp格式是如何保存图片的？文件内有哪些信息，以什么方式保存的？使用十六进制编辑器进行编辑验证。
  * 以比较直接的方式保存图片，不压缩，不加密
  * 图片中的每个点的颜色都是直接顺序存储在文件中的
  * 文件内有哪些信息
  * 图片的尺寸
  * 图片的颜色类型信息（单色/16色/256色/65536色/1670w[24bit/24位]色）

* gif格式是如何保存图片的？为什么图片放大能看到类似麻点的内容？
  * 压缩，会建立颜色表，从1670w色中抽取出256种颜色用在该图片中
  * 为什么图片放大能看到类似麻点的内容？
  * 因为只能有256种颜色，原图中未抽取的颜色只能过这256种颜色拼接混合出来

* 几种图片格式有什么主要的区别？合适的场景分别是？
  * jpg 适合存储照片，不支持透明
  * png 适合存储截图，支持256级透明
  * gif 动图
  * bmp
  * webp 各方面优于jpg的图片格式，适合移动端，同时支持透明
  * psd photoshop工程文件，存储图片创作中的所有信息，所以文件非常大，且浏览器无法识别该格式

* 将748367转换为5进制。
  * 142421432
# 6-29
## 思考题
* 什么是当前工作目录？
  * 即用户目前所在的目录，可以根据文件名访问文件。

* 什么是路径列表？如何设置？
  * 是一系列路径的集合，在环境变量内设置。

* interface一词有哪些含义？
  * 接口和界面。指发生联系或交换数据的接口。

* .bashrc文件是啥？
  * bash运行命令，在bash启动时会加载预先设置好的命令。

* 如何计算相对路径？
  * 数斜杠的个数。

* vi编辑器的编辑模式与常规模式是什么？如何切换？
  * 编辑模式可以任意输入文本，常规模式不可以。按Esc和i键。

* 如何用命令删除非空文件夹？
  * rm -r

* 阅读vim教程vimtutor。
  * 看了。
# 6-30
## git 代码仓库
* `git init` 在某个文件夹初始化一个仓库（一份代码只执行一次）

* `git config --global user.name "name"`  配置全局用户名（存在~/.gitconfig文件内）
  * `git config --global user.email "email"` 配置全局用户的电邮

* `git status` 查看当前状态（暂存区与工作目录）

* `git add <file>` 将文件添加到暂存区
  * `git add .`   将当前文件夹的所有文件都添加到暂存区
* `git restore <file>`  将文件从暂存区出来覆盖工作区对应文件
* `git commit -m "message"`  将暂存区的内容保存为一个版本（会输出简要汇总信息）

* `git log` 查看当前仓库的提交记录，如果多的话可以通过上下键翻页

* `git diff` 查看工作目录与暂存区的具体差异
  * `git diff --cached` 查看暂存区与最后一提交的具体差异
# 7-1
## VSCode 多光标快捷键
* 触发多光标方案：
  * Ctrl+Shift+L，高亮文本当中所有相同单词，选中并将光标移到词尾
  * Ctrl+D，选中下一个匹配的内容
  * Alt+鼠标点击，点击位置会多出一个光标
# 7-2
## git 版本回退
* `HEAD` 表示当前版本
  * `HEAD^` 表示上一个版本
  * `HEAD~n` 表示第n个版本
* `git reset --hard HEAD^` 回退到上一版本
  * `git reset --hard ffffff` 回退到指定版本
* `git reflog` 查看被放弃的版本号
## 撤销修改
* 撤销工作区修改 `git checkout -- file`
  * 用暂存区的同名文件替换工作区的
  * ！命令一定要包含中间的 `--`
* 撤销暂存区的修改
  1. `git reset HEAD <file>` 将文件取消暂存，放回工作区；
  2. `git checkout -- <file>` 再撤销工作区修改，和上一步一样
## 远程仓库
* `git remote add origin git@github.com:user/repo.git`
  * `origin` 远程仓库名，可以修改
  * `git push -u origin master` 推送命令，`-u` 参数将 `origin` 和 `master` 关联，之后可以简化命令
    * `git push origin master`
* `git remote -v` 查看所有远程仓库
  * `git remote rm origin` 解除本地和远程库绑定关系
## 从远程克隆和拉取
* `git clone git@github.com:nser/repo.git`
* `git checkout -b dev origin/dev` 克隆远程 `dev` 分支
* `git branch --set-upstream-to=origin/dev dev` 建立本地 `dev` 分支与远程` origin/dev` 分支的链接
## 分支管理
`HEAD` 是一个指针，指向当前所在的分支，可以任何分支之间切换
* `git branch` 查看 `*` 当前分支
* `git checkout -b dev` 新建并切换分支
* `git switch -c dev` 👆
  * `git branch dev` 只新建
  * `git checkout dev` 只切换
    * `git switch dev` 👆
* `git merge dev` 合并 `dev` 分支到当前分支
  * `git merge --no-ff dev` 禁用 `FastForward` 模式
* `git branch -d dev` 删除分支
  * `git branch -D dev` 强制删除未合并的分支
* `git log --graph` 合并分支图
  * `git log --graph --pretty=oneline --abbrev-commit`
## 储藏分支
* `git stash` 储藏当前工作区，以备未来恢复
* `git stash list` 查看工作现场列表
* `git stash pop` 恢复并删除
  * `git stash apply` 只恢复
    * `git stash apply stash@{0}` 当有多个工作现场时恢复指定的现场
  * `git stash drop` 只删除
* `git cherry-pick fffffff` 复制一个特定修改到当前分支
## 标签管理
* `git tag <tagname>` 对当前分支提交添加标签
  * `git tag <tagname> ffffff` 对过往提交添加标签
* `git show <tagname>` 查看标签
  * 标签总是和某个commit挂钩。如果这个commit既出现在master分支，又出现在dev分支，那么在这两个分支上都可以看到这个标签
* `git push origin <tagname>` 推送标签到远程
  * `git push origin --tags` 推送全部标签
* `git tag -d <tagname>` 删除标签
  * `git push origin :refs/tags/<tagname>` 删除远程标签
# 7-4
## HTML 标签
### 属性
* 每一个标签可以接受一个或多个属性
* 属性可以有值，也可以没有
* 属性名不区分大小写，属性值区分大小写的
* 属性的值一般使用双引号包起来
  * 也可以使用单引号
* 但当属性的值里没有空格，引号等特殊字符时，属性值是**完全可以**不用引号包起来的
* 如下列出一些，通用/全局属性(Global Attributes)，即可以用在所有元素上面且有实际意义
+ id属性，在不学js的情况下，也可以有地方要用到
  * 标签在整个页面唯一的值
  * 一般来说起成一个单一的单词，不以数字开头，没有空格
+ name属性，标签的名字，现在主要用在表单类标签上面
+ title属性，鼠标在上面时显示的tooltip文本
  * alt 属性，主要用在img标签上
  * 指定在图片加载失败的时候的替换文本
  * ![描述文本](url.jpg)
  * <img alt="描述文本" title="描述文本" src="url.jpg">
  * alternative 可选项，替补，或者
  * alternate
  * alter 修改
  * alert 警告
+ class="foo bar" 类别，类名
  * 空格分隔的单词列表（word,foo-bar）
  * comma/space separated list
+ style属性，用于给标签指定内联样式
+ tabindex
+ contenteditable(5)
+ data-*
  * <div isbn="567890">书籍详情</div>
* 文档：https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes
  * Google：html Global Attributes
* data-* 属性
* 如何在html内表示这些用来表示html自身的字符呢
  * 如<>="
  * &char_name;
  * &#decimal;
  * &#xHEX;
## 各个标签
### html
* 对于 xhtml 页面来说，根元素可以是其它标签
* 根标签 root element
* 一个页面只能有一个
* 没有的话，浏览器也会自动添加
<!DOCTYPE HTML>
<html></html>
{[() ()]}
### head
* https://github.com/joshbuchea/HEAD
* 头部标签，放一些与页面相关的“元信息”，比如：
  * 页面的编码方式
  - `<meta charset="utf-8">`
    + chartset：字符集
    + meta：元
* 编码方式又是一个很大的话题
* 一般的乱码都是因为编码方式引起的
* 页面的标题，即title标签
* 页面的图标，即浏览器标题栏左边显示的那个小图标
  - 页面图标可以用一个标签来设置
  + `<link rel(ation)="icon" href="http://www.baidu.com/img/favicon.png">`
  + 对于http://example.com/lksjdfasdfjasfd/asdfa/sdf/asd/fasdf/a.html
  * http://example.com/favicon.ico
  - 也可以不用一个标签设置，浏览器会自动读取网站根目录下的favicon.ico这个文件
    + 例如：http://www.baidu.com/favicon.ico
    * 比如页面的样式表
    * style/<link rel="stylesheet" href="a.css">
* 甚至页面可以在这里选择使用哪个引擎渲染
  * 国产很多双核浏览器支持这种模式
    - 浏览器普及
* <meta name="UA-X-Compatable" content="EDGE" />
  * cutting edge
  * bleeding edge
* 在移动端，还可以定义页面以多宽的尺寸渲染等
  - viewport,视口
  - <meta name="viewport" content="width=500" />
* head里的内容不会被显示在页面上
* 不存在的话，也会自动添加
### body
* 想要在页面中被显示出来的内容都放在这个标签里面
* 如果页面没有html或者body标签，浏览器会自动添加，并将页面内容包含在body里面
* 但浏览器同时也会将那些必须放在head里的标签放进head里面，比如title标签

  ```html
  <title>页面标题</title>
  <h1>一级标题</h1>
  <p>一个段落</p>
  ```

* 上面的代码会被浏览器解析为下面的结构

```html
<!-- <!doctype html> 这一行不会自动添加的 -->
<html>
    <head>
        <title>页面标题</title>
    </head>
    <body>
        <h1></h1>
        <p></p>
    </body>
</html>
  ```
* 同时，如果在body或者html标签的**结束标签之后**又出现了其它的标签，则之前的结束标签就会被认为无效，浏览器会自动添加结束标签

```html
<html>
    <head></head>
    <body>
        <div></div>
    </body> 这行会被认为无效
    <p></p>
    <script></script>
</html>
<div></div>
```

* 上面的代码相当于

```html
<html>
    <head></head>
    <body>
        <div></div>
        <p></p>
        <script></script>
        <div></div>
    </body>
</html>
```
### title
* 页面标题
* 仅支持纯文本，不支持嵌套其它标签
* 如果不出现在head内，将自动移到head内
* 出现多个的话，仅第一个生效
### h1-h6 标签
* header(标题) 1 到 6
* 一级到六级标题
* 默认情况下，标题上下会有一定的空白
* 比较传统的观点认为一个页面不能出现超过一个h1标签，原因是为了 SEO
* SEO 是什么？
  * Search Engine Optimism
  *  搜索   引擎    优化
  - 讲白了就是如何布置页面能让页面在搜索结果中尽量靠前
  - 手段有很多种，请各们各行了解，SEO本身也是IT行业里一个专业的职位
    + 如关键字
    + 页面被引用的次数（反向链接数量）
    * 交换链接
    + 使用https
    + 使页面的html更符合语义
* HTML5 中新增了 hgroup（即header group） 标签，大致用法如下：H5

  ```html
  <hgroup>
      <h1>三体</h1>
      <h2>一部人类文明的诗史</h2>
  </hgroup>
  ```

* 即当不同级别的标题显示在一起的时候可以用这个标签把hN标签归类
* 一般来说，这个标签可以替换以前使用div的场景
### p
* paragraph
* 语意是一个段落，当想要表达一段话时都可以使用这个标签
* 默认情况下也会有上下边距
### a
* anchor, 锚
* 语义是一个链接，链接地址写在  href（Hyperlink REFerence）属性里
* 可以链接到的类型非常多，而且一般来说是可扩展的
  * 绝对网址，fullpath
    * `<a href="https://jd.com/">京东</a>`
  * 页内特定位置跳转地址
      * `<a href="#pos1"></a>`
      * 例：https://html.spec.whatwg.org/multipage/grouping-content.html#the-dl-element
  * 其它页特定位置跳转地址
      * `<a href="http://jd.com/#footer"></a>`
  * 这个在书目的章节跳转在使用的比较多
* 相对路径
    * `<a href="https://baidu.com/">baidu</a>`
    * `<a href="a.html">baidu</a>`

    * `<a href=".././../a/b/../index.html"></a>`
    * `<a href="./index.html"></a>`
    * `<a href="../index.html"></a>`
      * http://a.com/a/b/c.html
        * http://a.com/a/b/index.html
        * http://a.com/a/index.html
    * `<a href="/index.html"></a>`
      * http://a.com/a/b/lkj/adsfa/sdf/c.html
      * http://a.com/index.html
* 电子邮件
    * `<a href="mailto:aaa@bbb.com"></a>`
    * `<a href="mailto:aaa@bbb.com?title=1&subject=2&content=3"></a>`
      * 需要在电脑安装邮件客户端
* 电话号码　tel:18611075877
  * 主要用在手机页面上
* QQ/taobao 临时会话
  * tencent://temp-chat?QQ=285696737
  * thunder://ghjk;adfklasdhfkweuhfasdlfk
* 等等等等
    - thunder://LKDJOIE7436239/
* 空的href属性 href=""  href="."
  * 链接到当前页面
    * 所以仅以#开头的值是中转到当前页面的特定位置
    * <img src="">
* 类似的，如果一个img标签的src属性为空，也将对应当前页面地址
* https://www.nczonline.net/blog/2009/11/30/empty-image-src-can-destroy-your-site/
* target属性
* 可以指定在哪个窗口打开链接
  * 几个特殊值,关键字
    * _blank，链接在空白的窗口显示，也就相当于新打开一个窗口了
    * _self，其实这个是默认值，就是在当前窗体打开
    * _parent，链接在父窗体显示
    * _top，链接在顶层窗体显示
* 自定义值
    * shopingcart，要求不能以_开头，出处：https://www.w3.org/TR/html-markup/datatypes.html#common.data.browsing-context-name-def
    * 这点等讲到iframe等标签时再说
      - _parent
      - _top这两个属性也是需要讲到iframe时再提起

* 在html5中，还有一个download属性
  `
    * 表示点击这个链接将下载链接对应的文件，而不是跳转到目标页面，下载的文件名以download属性的值来命名
* `<a href="xxx/jianai.pdf" download="简爱.pdf">点我下截《简爱》完整版</a>`
* 只能触发下载自己网站上的资源，只能在真正的网址上使用，即url以http开头
* 问题，如果同时有target=“_blank”，又有download属性，它如何行为呢？
  * 请自行测试
* 为什么要有这个属性呢？传统浏览器中，要触发下载，需要服务端的支持，给出特定的http头才会触发浏览器下载而不是打开对应的内容
  * 这个属性的出现可以让点击下载完全由前端来完成
  * img 标签
    * image
    * 表示一张图片
    * 用src(source)属性表示图片的地址
    * 同样也可以是绝对地址，相对地址
      * `<img src="http://www.baidu.com/logo.png" alt="" title="tooltip">`
      * `<img src="../abc.jpg" alt="">`
      * `<img src="/abc.jpg" alt="">`
      * <img srcset="a.jpg 1x, b.jpg 2x, c.jpg 3x">
      * hd/a.jpg
      * fhd/a.jpg
      * 1366*768
      * 19吋，1440*900
      * mac pro 1440*900  2880 * 1800 2k
      * 1280*720/800
      * 23， 1920*1080 -> 0.3mm 1
      * 4k 1920*1080 3840*2160
      * 5k 1920*1200 * 4
      * 2 笔记本屏幕
      * 3 手机
      * src指定的图片可以是浏览器支持的任意图片格式
      * jpg/jpeg,png,bmp,gif,webp,svg,ico
      * 注意psd格式应该是不支持的，因为它是photoshop专有的格式，支持它需要大量的代码而且psd格式的文件一般很大，一般都在几十M上下
* 同时，用 alt 属性表示图片在加载失败时的替换文本
    * 类似于markdown中图片的替换文档`![加载失败的替换文档](image source)`，事实上两者基本上是等同的
    * alt 的全程是 alternative
        * 自己查询这个单词的意思，就明白为啥用这个词了
        * 键盘上的Alt键是这个单词的前缀，即 alter
* 可以使用 width 和 height 属性定义图片的宽和高
    - 只写一个的话另一个会根据图片原始比例计算出来
    - 图片一般来说有自己的宽高（natural width/height）
    - 但是图片加载往往需要时间，而图片在加载完成之前浏览器是不知道其宽高的，所以就会产生页面抖动的问题
    - 所以一般会在标签上把宽高写出来，这样图片加载过程中页面就不会抖动了
    ```
    * usemap="#themap"
    * <map>
          <area title="xxxx" href="xxx" shape="rect" coords="0,0,100,100">
          <area title="xxxx" href="xxx" shape="circle" coords="0,0,100,100">
          <area title="xxxx" href="xxx" shape="poly" coords="0,0,100,100">
      </map>
    ```
    - 可以让图片不同区域对应不同的链接
    - 后面说到map标签后再说
### span
* ```<span class="price">10.00</span>```
* ```<p> aaa <strong> bbb </strong> ccc </p>```
* 是一个没有明确语义(通用语义)的标签
* 一般来说想要给特定的内容加样式时可以用一个span标签将内容包起来
  * 后面学到css就知道了
### div
### br
  * break
  * 换行
  * 自闭合标签
  * `<br>`
### hr
  * horizontal
  * 水平分隔线
  * 自闭合标签
  * 强行写做 `<hr>some text</hr>` 的话里面的内容会被移出标签
    - 可以理解为没有</hr>标签
### base
- `<base href="页面中所有相对路径的基准地址" target="页面中所有链接的打开位置">`
+ href属性表示页面中所有**相对路径**的基础路径
  * 一定要以/即目录结尾
    - `<base href="https://www.baidu.com/abc/">`
    - `<base href="/">`相当于`<base href="https://www.baidu.com/">`
+ target属性表示页面中**所有链接**的打开位置
  * 当然，可以在页内的a标签中用它自己的target属性覆盖用base标签设置的全局打开位置
- 有些框架等可能会利用这个特性
### font/blink/marquee
* `<blink> lsk <font>jf</font> dowe </blink>`
* `<marquee> foo </marquee>`
  * deprecated 不推荐使用
  * obsolete   已废弃
  * 字体
      - 用size属性表示大小
      - face属性表示字体  fontface
      - color属性表示颜色
      * `<font size="25px" face="幼圆" color="red"></font>`
  * 已废弃
  * 早些年不用css时可以使用这个标签指定字体等
  * 所有已废弃的标签将不再提及
### em
  * emphasis
  * 语义为**强调**
### strong
  * 语义也为强调
  * 但强度跟em不同，strong的强调更重一些
### b bold
  * 只是样式上加粗
### u underline
### i italic
  * 多数网站会这个标签来表示图标
  * italic，斜体的，一般编辑器（如word）的斜体按钮就是用的一个斜着的I图标表示
  * 在以前，这个标签就是表示斜体文字的
  * 但html5中对其语义进行了明确
      * 用来表示由于某些原因需要与普通文本区分的文本
  * 默认情况下为斜体
  * 因为跟icon这个单词的首字母一样，很多人/框架/库也用这个标签来表示图标
      - http://fontawesome.io/
          * `<i class="fa fa-star"></i>`
