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
  * `![描述文本](url.jpg)`
  * `<img alt="描述文本" title="描述文本" src="url.jpg">`
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
  ```
  <!DOCTYPE HTML>
  <html></html>
  {[() ()]}
  ```
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
    * `style/<link rel="stylesheet" href="a.css">`
* 甚至页面可以在这里选择使用哪个引擎渲染
  * 国产很多双核浏览器支持这种模式
    - 浏览器普及
* `<meta name="UA-X-Compatable" content="EDGE" />`
  * cutting edge
  * bleeding edge
* 在移动端，还可以定义页面以多宽的尺寸渲染等
  - viewport,视口
  - `<meta name="viewport" content="width=500" />`
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
# 7-5
### `<!-- 注释 -->`
- 没有基础的同学可能对注释这个概念有点陌生
  + **注释是对程序本身的解释，几乎不会对程序的行为造成任何影响**
    * 说几乎，是因为有些注释还是会对程序有一些影响
+ 几乎任意语言里都有注释
  * C/C++,JS,PHP，java等语言//   ,  /*  */ comment block  c style
  * bash 脚本（即命令行脚本），python
    - 以#做为注释
  * css
    - 以/**/内的内容为注释
    - xcolor: red;
### html entity
- 转义(escape)：html entity HTML实体
  * &name;
  * &#number; 十进制数，`&#25105;` 我
  * &#xHHHH; 十六进制数, `&#x6211;`
    * Hexdecimal
  * Unicode
  * 常见具名html实体：
    * `&nbsp;` non-breaking space 160号空格
    * `&amp;` &符  ampersand
    * `&copy;` 版权符
    * `&lt;` 小于号 lettle then
    * `&gt;` 大于号 greater then
    * `&quot;` 双引号 quote
    * `&apos;` 单引号
  * 文档：
    * Google： html entity
    * https://dev.w3.org/html5/html-author/charref
    * http://www.w3school.com.cn/html/html_entities.asp
    * http://www.w3school.com.cn/tags/html_ref_entities.html
    * [ square bracket ]
    * { curly braces } mustcache
    * ( parentheses )
    * ; semicolon
    * : colon
    * , comma
    * . period
    * / slash
    * \ backslash
    * ? question mark
    * \+ plus sign
    * \* times star asterisk
    * | vertical  | bar ||||||
    * ! exclaimation
    * ^ caret
    * \# hash
    * `~~~
    * $ dollar
    * @ at
* 对空白字符的忽略
* 默认情况下浏览器忽略文字与文字之间多于一个的空格，换行符会被全部忽略
  * 当然css可以改变这种行为，后我们会看到
### 可访问性 accessibility
* 在各个设备上访问/对各种人群可访问/视障/听障
* 读屏软件
* windows 高比对度主题
* a r i a / role
  * accessibly rich Internet Application
  * 网页应用程序
  * role属性提示浏览器当前元素是一个何种视觉元素
    * role=""
  * aria-xxx="yyy"提示浏览器当前视觉元素的状态或其它信息
### pre
* pre formatted
* 表示有预定义格式的文本
    * 里面的内容的回车跟空格都会被保留
* 本来有个width属性，表示每行最多的字符
    - 本来支持度也不好，然后在html5中被弃用了，因为可以用css来更精确的控制
* 常与code标签 `配合` 使用，用来在`网页`里显示高亮过的代码
  * `<pre><code class="">code goes here</code></pre>`
  ```js
  var a = 8
  <p>
    foo
    <code>
      bar
    </code>
  </p>
  ```
### 列表类标签
- ol，ul
    + Ordered List, Unordered List
    + 其直接子结点必须只能是li标签 list item
        * li内可以是任意其它标签
    + 默认会在每多一层级的列表中缩进
    + 并带有列表项标号，有序和无序的
    * 多个同类项的重复，就应该使用ol/ul标签
    * LISP List Procressing SICP
    * 黑客与画家
- dl
    + Description List / define list
    + dt
        * Description Term
    + dd
        * Description Description
    + 一个列表项是**一个dt**和**一个或多个dd**一起算一组
    + 此标签与ol/ul有些区别，在于
        * 一个dt可以对应多个dd
    ```html
    <ul>
      <li>
        <span>老师</span>
        <span>谢然</span>
      </li>
    </ul>
    <dl>
        <dt>老师</dt>
        <dd>谢然</dd>

        <dt>学生</dt>
        <dd>张三</dd>
        <dd>李四</dd>
        <dd>王五</dd>
    </dl>
    ```
### form表单标签

##### input
- https://www.google.com.hk/search?q=invalid+inentity+escape+in+regular+expression
- https://stackoverflow.com/questions/36953775/firefox-error-unable-to-check-input-because-the-pattern-is-not-a-valid-regexp
- https://www.fxsitecompat.com/en-CA/docs/2016/input-pattern-now-sets-u-flag-for-regular-expressions/
- https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/Input
* 属性
+ action
    * 表单提交的地址
+ target
    * 行为类似a标签的target
+ method
    * 表单提交方式
        - get
            + 将表单字段拼成querystring
                * 什么是querystring？
                    - http://abc.com/?a=1&b=2&c=3
        - post
            * 这个等学到http再说
+ enctype，编码方式
    * 在讲到http的时候再谈
+ type属性的各项值
    * text
        - 文本
    * password
        - 密码
    * checkbox
        - 复选框
        - 以name相同分组
        - checked属性表示默认选中
    * radio
        - 单选框
        - 剩余同上
    * file
    - accept
        + 可以接受的文件类型
        + `<input type="file" name="" id="" accept="image/*,text/*">`
        * MIME Type 媒体类型 Multipurpose Internet Mail Extensiion
        + `<input type="file" name="" id="" accept=".jpg,.png,.gif,.jpeg,.webp,.exe" value="c:/user/xieran/desktop/a.pdf">`
        * http://wwww.a.com/favicon.ico
    - 安全问题
    - multiple
        + 是否支持多选文件
    * .txt  text/plain
    * .js   application/javascript
    * .css  text/css
    * .html text/html
    * .png  image/png
    * .jpg  image/jpeg
    * .gif  image/gif
* hidden
    - 隐藏的输入域
    - value设置其值
    - name设置名字
* 为以下四个值时，都表现为按钮的样式，按钮上的文字需要用value属性来设置
* image
    - 从功能上讲是一个表单提交按钮
    - 从形态上看是一个图片
    - 此时需要使用src属性指定图片的地址
    - 现在基本上不这么用，之所以有这个用法，是以前不用js时想做出漂亮的按钮时，需要这么用
    - 在html5中，可以在这种标签上给定width跟height，类似img标签相应的属性，src，alt
* button
* submit
    - 单击时会触发表单的提交
* reset
    - 单击时会重置表单为初始状态
* **以下为html5新增属性值**
* number
    - 输入数字
    * e,.,-
    * -3.14e-8
    *
* email
    - multiple
    - 使用半角逗号分隔每个地址
* date
* datetime-local
* time
* week
* month
* url
  * protocal://user:password@domain:port/a/b/c/d.html?a=b&c=d#sldjfoiwjeofij
  * 百度.中国
* tel
* range
    - min，4
    - max，10
    - step，2
* color
    - value将返回十六进制颜色#abcdef
* 不能识别的值，当做text来处理
##### input的其它属性
- value
    + 为按钮形态时设置上面的文字
    + 为输入框时设置里面的默认内容
      * datetime-local
        * https://zh.wikipedia.org/wiki/ISO_8601
- name
    + 很重要，表单提交时，这个域/字段/框/FormControl的名字
    + 同时，在radio和checkbox阵列里，name相同的元素被分在一组里


- disabled
    + 无值的属性
    + 禁用这个输入域
- required
    + 设置这个输入域为必填项
    + 不填的话无法用**正常手段**触发表单提交
- maxlength
    + 为文本输入框时设置输入的最大长度
- minlength
    + 同上，但为设置最小长度
    + 不过兼容性不太好，不少浏览器没有实现
        * 有点矛盾，不填的时候是空的，当然会非法
- placeholder
    + 占位符
    + 提示性文字，一旦输入内容就消失
- autofocus
    + 自动获得焦点，即页面加载完后光标自动在这个元素内
- tabindex
    + 按tab键在不同输入域之间跳转时的顺序
    + 会往顺序更大的元素跳
    + 为-1的话会跳过那个元素
- button
  + type属性
      * 不写type属性的话，默认为submit
          - 即：无type的button的type属性默认为submit
      * `<button type="reset/button/submit">Submit</button>`
      * button
          - 常规按钮，功能上与input[type="button"]一样
      * submit
          - 提交按钮，功能上与input[type="submit"]一样
      * reset
          - 重置按钮，功能上与input[type="reset"]一样
  + 与`<input type="button" name="b" value="lksjdf">`的区别
      * input的button只能在按钮上显示纯文字
      * 而button标签可以在按钮上显示其它内容比如图片（即嵌套其它标签），文字也可以设置不同颜色等
- label 标签
  + 一般与checkbox及radio一起用，以扩大这两个按钮的可点击区域，提升用户体验。当然，也可以跟其它元素一起用，不过一般没必要（比较典型的是与input:file一起用）
  - for属性
      + 为想要被扩大点击区域的元素的id，不带井号
      - 细节：在ie8及以下不能用于displaynone的表单元素，可能是因为 not focusable
      - 表单元素嵌套在label的时候可以不用for属性
        ```html
        <form action="">
          有for的用法
          <label for="oneid">One</label>

          <input onclick type="text" id="oneid">

          不用for的用法
          <label>
            <input type="checkbox"> 男
          </label>
        </form>
        ```
  - 如下怎么算呢？
    ```html
    <input id="a">
    <label for="a"> lllll
      <input type="text">
    </label>
    ```

  - 典型的坑，两次点击，等学了js后再谈
- select name="sel"
  + 下拉选择框
  + 属性
      * multiple
          - 无值属性，表示多选，多选时就不是下拉的样式了
  + 另外此标签在不同的系统里面样式差别很大，而且它的样式一般来说是取自系统自带的，所以很难被css控制
      * 所以一些对 ui 要求比较高的网站都选择用其它元素模拟下拉框
          - 例：小米路由器
  + size属性控制默认显示的数量，也即它的尺寸
* option
  * value
      - 选择了该项目后它所属的select元素的值
  * selected
      - 默认被选中
  * disabled
      - 表示该项被禁用
  * hidden
      - 表示该项被隐藏
  - 以上三个属性均无值
* optgroup // hgroup  colgroup
  - 给option分组
  - 用label属性表示这个分组的名字
  - 无法被选中，只选择option
  - 有一个disabled属性，如果设置了这个属性，整组标签都会被禁用
  ```html
  <select>
      <option value="1">1</option>
      <optgroup label="这是一个分组" disabled hidden>
          <option value="01">01</option>
          <option value="02">02</option>
          <option value="03">03</option>
          <option value="04">04</option>
          <option value="05">05</option>
      </optgroup>
  </select>
  ```
  - 兼容性不确定，因为我没用过mac
- textarea
  + 多行文本输入框
  + 两个特殊属性
      * rows="3" 行
      * cols="20" 列  column
    + 不过现在也不常用，一般都用css来控制了
- fieldset 字段组 用来把 一组 输入域 放在一起的。
  + field就是字段的意思，就是说一个表单输入域（输入框）
  + 这个标签用来给输入域分组，所以叫set
      * set本来就是组的意思
  + 如果只是分组，完全可以用div等标签
      * 那这个标签有什么用呢？
      * fieldset有个disabled属性，如果它有了这个属性，其内的所有输入域都将被禁用，类似optgroup
          - 在某些场景下是非常好用的
- legend
  + 只能作为 field set 的子元素，用来标识这组输入域的名字，基本上没有其它用处
      * 而且在有了css之后，这个标签基本也没有用武之地了
# 7-6
## table
- 这个标签以前经常用于做布局
    + 什么是布局？即页面大区块的排列和摆放
    + 为什么呢？因为table都是方方正正格子，了解后很容易控制
        * 语义很差
        * 可读性很差
        * 可维护性也很差 maintainable
        * 可访问性
    + 但现在有了 css 之后，基本上只用table来显示数据，即表格本来的作用
    + 熟悉 DIV+CSS 布局 JD Job Description
* caption
    - 表格标题
* thead
    - 表头
    - 做为table的直接子元素
    - 只能有一个
    - 只有一个的情况下，即使出现在tbody的后面，其内容也会显示在tbody的前面
    - 非要写多个的话，第一个以外的会当做tbody来处理
* tbody
    - 表格主体
    - 做为table的直接子元素
    - 可以有多个
* tfoot
    - 表尾
    - 做为table的直接子元素
    - 只能有一个
    - 只有一个的情况即使出现在tbody的前面面，它的行也出现在tbody的后面
    - 非要写多个的话，第一个以外的会当做tbody来处理
* tr
    - table row cell
    - 表格行
    - 可以直接做为table的子元素，会被放入创建的tbody里面
    - 或者做为上面三个标签(thead/tbody/tfoot)的子元素
* th
    - table header cell
    - 用在表头单元格
    - 文字默认为加粗
    - id用于被td元素引用以表示td所属的标题是哪一个
        + 看例子
* td
    - table data，表格数据单元格
    - headers
        + 表格头，值为某th的id，以表示这个数据的名称
            * 方便读屏软件
        + headers的值可以是多个以空格分隔的th标签的id的值，用法可能是th或td单元格跨行或跨列了
    - 跨行跨列的单元格
        + col span 跨列
        + row span 跨行
        + 错误的示范：
        + http://www.splaybow.com/html-table-rowspan-colspan.shtml
        - http://jsbin.com/nikifi/edit?html,output
        - http://jsbin.com/yehecez/edit?html,output
        - http://jsbin.com/susomoh/1/edit?html,output
* col/colgroup 标签
    - colgroup
        + 用来分组col标签
        + span属性，表示选择多列表格
        + 有span时，不可再有子的col元素
        + 大部分属性同col元素
    - col
        + 用来设置表格列的属性和样式
        + span属性，表示选择多少列表格列，默认为1
    - 可以单独使用，也可以被colgroup分组
      ```html
      <table>
          <caption>表格标题</caption>
          <col>
          <col>
          <colgroup></colgroup>
          <colgroup></colgroup>
          <colgroup bgcolor=red>
              <col>
              <col bgcolor=navy>
          </colgroup>
          <tbody>
            <tr bgcolor="red">
              <td></td>
              <td></td>
              <td></td>
              <td></td>
            </tr>
          </tbody>
      </table>
      ```
    - 必须出现在caption后面，thead/tbody前面
    - 很多属性不支持了
        + 而w3schools上面还列着
        - http://www.w3school.com.cn/tiy/t.asp?f=html_col_test
    * 其它
    * border-spacing CSS属性, spacing是重合的
    * cellspacing=0
    * tr或者td or th不能有其它并列标签,否则会识别错误
        * 有些元素的 position:relative 无效，见下
        * https://stackoverflow.com/questions/6746175/html-tr-tag-and-positionrelative
        * box-shadow 也不支持某些类型的元素
        * https://stackoverflow.com/questions/10874985/box-shadow-on-table-row-not-appearing-on-certain-browsers
## map
  - 不是“地图”标签，是“映射”标签
  - name属性
  - 如果设置id属性的话，id跟name属性值必须一样
      * <input type="radio" name="a" id="a1">
        <input type="radio" name="a" id="a2">
        <input type="radio" name="a" id="a3">
        <input type="radio" name="a" id="a4">
        <input type="radio" name="a" id="a5">
* area
    - 必须做为map的子元素
    - w3school上的错误示范：http://www.w3school.com.cn/tags/att_img_usemap.asp
    - 属性
        + href
        + target
        + alt
        + 以上三个属性同a标签
        + shape
            * rect(angle)，矩形
                - x1,y1,x2,y2
            * circle，圆形
                - cx,cy,r
                - 圆心x，圆心y
                - 半径r
            * poly(gon)，多边形
                - 至少6个值，表示一个多边形的若干个顶点
        + coords coordinate
            * 对应shape的几种图形的坐标
        + code
          ```html
          <img title="image title" src="https://drscdn.500px.org/photo/174778125/m%3D1170_k%3D1/2841ccf2a3720e8e794a6a6930f6ff2c" width=300 usemap="#somemap" alt="">

          <map name="somemap">
            <area shape="rect" coords="55,108,205,200" href="https://www.mi.com/" alt="ieksoef" title="abc" target="_blank">
            <area shape="circle" coords="133,262,90" href="" alt="">
            <area shape="poly" coords="57,82,8,265,163,397,225,256,187,83" href="" alt="">
          </map>
          ```
## iframe
- inline frame 内联窗体
- 必须有开始标签和结束标签
    + 可以在标签之间写上不支持此标签时的退化（fallback）内容
* 各种属性
    - src
    - name
        + 提及a标签的target属性
          * _self, _blank
          * _top, _parent
          * 自定义名字
        * 以前常用来做导航
        * base, a, form, img + map>area
    - sandbox
* webview
* 它的跳转记录也会存在于浏览器的前进后退的记录里面
* code
  ```html
  <p>this is frame 4</p>
  <iframe src="frame3.html" frameborder="1">
    your browser don't support iframe
  </iframe>
  <p>this is frame 4 </p>
  ```
  ```html
  <p>this is frame 3</p>
  <iframe src="frame2.html" frameborder="1"></iframe>
  <p>this is frame 3 </p>
  ```
  ```html
  <p>this is frame 2</p>
  <iframe src="frame1.html" frameborder="1"></iframe>
  <p>this is frame 2 </p>
  ```
  ```html
  <a href="http://mi.com/" target="_top">mi</a>
  ```
## frameset&frame
- rows/cols="10%,50px,*"
- noframes
- code


  ```html
  <iframe src="">
    <p>您的浏览器不支持iframe，请升级</p>
  </iframe>

  <frameset rows="100px,*,100px">
    <frame src="https://www.jd.com/">
    <frameset cols="50,50">
      <frame src="https://www.jd.com/">
      <frame src="https://www.jd.com/">
    </frameset>
    <frame src="https://xieranmaya.github.io/">
  </frameset>

  <noframe>您的浏览器不支持框架</noframe>
  ```

  ```html
  <frameset>
      <frame>
  </frameset>
  <noframes>您的浏览器不支持框架</noframes>

  <canvas>
    <p>no supported</p>
  </canvas>

  <script>
    var a = 8
  </script>
  <noscript>your browser dont support javascript!</noscript>



  <iframe src="" frameborder="0">
        <p>no supported</p>
  </iframe>

  fallback 退化方案
  degrade 降级方案
  backdrop 备用方案

  <script>
      alert()
  </script>
  <noscript>
    <p>woiejflksdjafoiw</p>
  </noscript>
  ```
## 语义化
* div division 没有语义的标签
  ```
    <div class="footer"></div>
    <div class="header"></div>
    <div class="sidebar"></div>
    <div class="navigation"></div>
    <div class="wrapper container">

    </div>
    <div class="content"></div>
    <div class="main"></div>

    <article></article>
    <div class="article"></div>
    ```
  * HTML5 新增的一些语义标签
  ```
      - <article></article>  <div class="article"></div>
      - section  div
      - aside
      - header
      - footer
      - nav(igate)
      - main
      - template 模板
      <table>
      </table>
      - <textarea>
          <span></span>
          <h1></h1>
        </textarea>
  ```
  * 其它常见标签
    - sub
    - sup
    - code
      + 与pre不一样，不过一般与pre一起，用来显示代码块
      + `<pre><code>code  goes here</code></pre>`
* script
    - `<script>js goes here</script>`
    - `<script src=".././.././less.js">js not allowed</script>`
    - 遇到`</script>`就结束
* style
    - `<style>css goes here</style>`
    - `<style src='a.css'>css goes here</style> xxx`
    - `<link rel="stylesheet" href="a.css">`
* 多媒体标签
    - video 视频
        + mkv xxx
        + rm rmvb xxx
        + avi xxxx
        + mp4 supported h264 / h265
        + m3u8 supported
          * m3u8 list
          * xxxx.m3u8
            * 0 6   http://wa.com/a.mp4
        + webm webp
        + mpg  jpg
    - audio 音频
        + mp3 ogg m3u8 wmv wav
    - usage
      ```html
      <video autoplay loop preload controls>
          <source src="a.mp4" >
          <source src="a.m3u8" >
          <source src="a.webm" >
          您的浏览器不支持video
      </video>
      ```
    - flv.js
    - 自动播放属性 autoplay
    - 循环属性 loop
    - 预加载属性 preload
    - 控制条属性 controls
* object 东西，对象
    * type属性
      * MIME Type image/png, video/webm
      * application/pdf
    * iframe
    * pdf
    * svg,img
    * flash
    * 300*150 跟iframe一样
* embed 嵌入
* canvas
    - 画布
    - 必须有结束标签，内部写上不支持canvas的浏览器的提示性文字
        + `<canvas><p>您的浏览器不支持canvas</p></canvas>`
    * width/height 属性与css的width/height是不一样的
        * 如果不同的话图片会被拉伸
    * 默认是透明的
* progress
    * max
    * value
    * http://www.zhangxinxu.com/wordpress/2013/02/html5-progress-element-style-control/
    * 下面这篇更好
    * https://css-tricks.com/html5-progress-element/
+ 标签文档
  * https://developer.mozilla.org/en-US/docs/Web/HTML/Element
    * tt
    * kbd  keyboard
    * address
    * q
    * blockquote

+ doctype Document Type Delclearation
  ```
  document type declearation
  <!doctype html  //STRICT/html.dtd >
  <!DOCTYPE html> 让浏览器以最新的标准来解析这个页面
  ```
  * html5????   CSS(CSS2 + CSS3)
  * H5   C3
    * 对于外行来说
      * 往往指的很炫酷的网页
  * HTML5
    * 到目前为止，所有的前端技术集合
      * es6，css3，html5，新的浏览器功能（API）
  * 如果不写doctype声明，页面在IE浏览器下会以quirkmode（怪异模式）渲染
    * IE6时引入
    * 最主要的区别是css盒模型计算方面
+ meta
* encoding
* viewport
* keywords `<meta name="keywords"  content="小米，大米" >`
* author  `<meta name="author"  content="damiao" >`
* description
+ link
* 引入 css
* 引入 页面的图标
  * favicon.ico
+ 语义化
* 语义化做的好的页面能够方便人与机器的理解
  * maintainable能够让团队的后来者更易于维护代码（可维护性）
  * 能够让页面在搜索引擎的结果中更靠前（让机器更易理解）
* 合适的内容选用合适的标签
* 合理使用h，p，列表，表格，div，span及html5新增语义标签
* 使用合适的嵌套
  * `<button><p></p></button>`
  * `<p><div></div></p>`
  * `<a><button></button></a>`
* 给元素命名上合适的类名及id名称
* css裸奔节
* 标签的分类：
* 曾经：
  * 块级元素 h1234, div, p, ul,li
  * 行内元素 span a em strong i b sub sup
* 现在：
  * https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Content_categories
* div > a > div > p > span > a
* div span a b u strong em
* ul li ol dt dl dd table*
* form input textarea
* img
```
<div>
  <a href="">
    <div></div>
  </a>
</div>
```
读屏软件可以理解/识别传统软件的常见视觉元素
* role 与 aria-*
- 富文本   纯文本
* accessible rich Internet Application （可访问的 富 互联网应用）
* rich text format
* 视觉元素
* 由来
  * UI控件/组件
  * web app
    * rich application
    * 任何能用js实现的软件最终一定会用js实现
* role
  * role="textbox"
  * role="listbox" -> select
  * role="option" -> option
  * role="progressbar" -> progress
  * role="tabs" -> 选项卡
  * role="dropdown" -> 下拉框
* aria-*
  * aria-disabled="true"
  * aria-checked="true"
  * aria-valuenow="true"
  * aria-valuemax="true"
  * aria-valuemin="true"
  * aria-readonly="true"
  * aria-selected="true"
* `<div role="checkbox" aria-checked="flase">`
- `<input type="checkbox" >`
* 一般来说，role与aria-*用在非语义标签上
  * 如div，span，li，a等
  * 不用在如nav，article，footer等标签上
    * 以及select，input
* 文档：https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA
# 7-7
## CSS 选择器
- 类选择器 `.classname`
- ID 选择器 `#idname`
- 属性选择器 Attribute
  - `[attr]`
    - 选择有 attr 属性的标签
  - `[attr="value"]`
    - 有 attr 属性，且值为 value
  - `[attr^="value"]`
    - 值以 value 开头
  - `[attr$="value"]`
    - 值以 value 结尾
  - `[attr*="value"]`
    - 值包含 value
  - `[attr~="value"]`
    - 值包含以空格分隔的 value
    - `[class~="classname"]` 基本等价于 `.classname`
  - `[attr|="value"]`
    - 值以 value 或者 value- 开头
    - 常用于匹配语言代码：`en-US`
  - `[attr operator value i]`
    - 忽略大小写
- 伪类选择器 Pseudo-classes
  - 鼠标悬停 `:hover`
  - 鼠标点击未松开 `:active`
  - 激活焦点 `:focus`
  - 未点开的链接 `:link`
  - 点开过的链接 `:visited`
  - 一组兄弟元素中的第一个元素 `:first-child`
  - 父元素的最后一个子元素 `:last-child`
  - `:nth-child(an+b)`
    - 0n+b 匹配第 b 个元素
    - 1n+0 匹配第 n 个元素
    - 2n+0 或 even 匹配偶数
    - 2n+1 或 odd 匹配奇数
    - 3n+4 匹配位置为 4、7、10、13...的元素
  - `:nth-of-type()` 具有一组兄弟节点的标签，用 n 来筛选出在一组兄弟节点的位置
    - 和 `:nth-child()` 类似，不过只筛选相同元素，不是相同的元素会被跳过且不参与计数
- 复合选择器
  - `div.foo.fob[foo="bar"][title="bar"]#baz:hover:active:first-child`
    - 👆选择一个 div 元素，具有 foo 和 fob 类、含有 foo 属性且值为 bar、含有 title 属性且值为 bar、含有 baz ID、且当鼠标悬停，点击不松开时、是一组兄弟元素中的第一个元素
    - 不可有空格
- 组合器
  - `A B` 选择 B 且 B 属于 A 的后代
  - `A > B` 选择 B 且 B 属于 A 的直接子代
  - `A ~ B` 选择 A 之后的所有 B，A B是同层级兄弟元素，不必紧邻
  - `A + B` 选择 A 之后的一个 B，A B是同层级兄弟元素，且紧邻
    - 此选择器会循环查找，即当两个兄弟元素相同时，会再一次循环查找
  - `A, B` 同时选择所有 A 和 B
# 7-8
## 选择器的优先级
- 格式：四元组👇
  - `(0, 0, 0, 0)`
- ID 选择器，如 `#foo`、`#bar`
  - `(0, 1, 0, 0)`
- 类、属性、伪类选择器，如 `.foo`、``[]`
  - `(0, 0, 1, 0)`
- 元素选择器、伪元素选择器，如 `p`、`span`
  - `(0, 0, 0, 1)`
- 内联样式 `inline style`
  - `(1, 0, 0, 0)`
  - 写若 `<p style="color: green;">`
- 下列不参与优先级计算
  - 连接符 `>` `+` `~`
  - 通配符 `*`
- `!important` 优先级最高
  - 写若 `p {color: red !important;}`
- 继承
  - 没有优先级
- 优先级大致顺序
  1. 用户自定义 `!important`
  2. 网站作者定义 `!important`
  3. 网站作者普通样式
  4. 用户自定义普通样式
  5. 默认样式 `User Agent Style`
- 优先级若一致，后出现的覆盖前面
## 值、单位
- 数字
  - `0.n` 可以写为 `.n`
- 百分比
  - 百分比和纯数字不可互换
- 颜色
  - RGB
    - red, green, blue, cyan
    - `#ffffff`
    - `#abc -> #aabbcc`
    - `rgba(0->255, 0->255, 0->255, 0->1)`
    - `rgba(r%, g%, b%, a%)`
  - CMYK
  - HSL, HSV
- 长度
  - 绝对长度／物理长度
    - in
    - cm
    - mm
    - -moz-mm
    - pt `point` 72 分之一 inch
    - pc `pica` 6 分之一 inch
  - 相对长度
    - px `pixel`
    - em 在 font-size 中使用是相对于父元素的字体大小，在其他属性中使用是相对于自身的字体大小，如 width
    - rem 根元素的字体大小
    - vw 视窗宽度的 1%
    - vh 视窗高度的 1%
    - vmin 视窗较小尺寸的 1%
    - vmax 视图大尺寸的 1%
    - calc(计算)
- 角度
  - deg 角度
  - rad 弧度
    - `π rad = 180 deg`
  - turn 圈
    - `1 turn = 360 deg = 2π rad`
  - `transform: rotate(180deg);`
- 时间
  - s, ms
- URL
  - `import url("aaa.css");`
  - `background-image: url(a.png);`
  - `url("protocol://a:b@server/pathname?a=b&c=d")`
- CSS 关键字
  - `display: none block inline inline-block table table-cell;`
  - `background-color: currentColor;`
  - `border-style: solid/dotted/dashed/ridge;`
- 字符串
  - `content: 'ffoo\6211oo'  "wosdf  iejf -=owiejf"   "jowiejfo";`
- 取属性的值
  - `content: attr(href);`
  - `transform: rotate(30deg) skew(50deg) matrix(1,2,3,4,5,6);`
## 字体
- `body {font-family: sans-serif;}`
  - 自动选择无衬线字体
- `h1 {font-family: "MicroSoft YaHei";}`
  - 使用指定字体
- `h1 {font-family: "Helvetica", "微软雅黑", sans-serif;}`
  - 字体回退
- 字重 `font-weight`
  - normal
  - bold
  - bolder
  - lighter
  - 100 - 900
  - inherit
- 字号 `font-size`
  - xx-small = 12
  - x-small = 14
  - small = 15
  - medium = 18
  - `large`
- `font-style`
  - `normal`
  - `italic`
  - `oblique`
    - 是 `italic` 的回退
- `font-variant`
  - `normal`
  - `small-caps`
    - 把小写字母显示成小号的大写字母
- `font: [<font-style> || <font-variant> || <font-weight>] <font-size>[ / <line-height>] <font-family>;`
  - `font: small-caps bold 20px / 1.2em 明体, serif;`
  - 前三个的顺序不重要
      + border:red  solid 1px;
  - 如果前三个的随便哪一个值为normal，则可以省略
  - `line-height`可以省略，但如果出现，必须加/并且出现在fz的后面
  - fz跟ff必须出现，而且顺序也是这个顺序，不能乱
- 文本相关
  - 缩进 `text-indent: 2em/5%`
    - 用`text-indent: -99999px`来把标签里的文字隐藏，然后用背景图片“替换”标签内容
    - -2em 这种可以实现首行悬挂
    - 2em 则可以实现首行缩进
  - 文字水平对齐 `text-align`，`text-align-last`
    - `left`
    - `right`
    - `center`
    - `justify`
  - 文字垂直对齐 `vertical-align`
    - `line-height` 行高
      - `content-area`
      - `inline-box`
    - `vertical-align` 这个属性适用于【内联元素】
      - `baseline` 默认值
        - 让元素的基线与其父元素行框的基线对齐，如果一个元素没有基线，如img，input，则让其底部与外面的文字对齐。即使行框没有文字也是一样。
      - `sub` 元素的 baseline（或底部）会比父该行文字的 baseline 低
      - `super` 同上，元素的 baseline 比该行内容的 baseline 要高
      - `bottom` 目标元素的底部跟这一行的底部对齐
      - `top` 目标元素的顶部跟这一行的顶部对齐
      - `text-top/text-bottom`
        - 元素的顶/底部与文字的顶/底部对齐
      - `middle` 并不是垂直居中，而是把【元素的中间】与baseline上面0.5ex（即四分之一em）对齐
  - `word-spacing` 词间距
  - `letter-spacing` 字间距
  - `text-transform：uppercase/lowercase`
    - 全部文字大写／小写
    - `capitalize` 首字母大写
    - 本属性的效果先于 `font-variant` 执行
  - `text-decoration`
    - underline 下划线 overline 上划线 line-through 删除线
    - 值得注意的是子元素没有办法去掉由父元素留下的各种线
    - 另外线的位置，粗细，样式都不能指定
    - ```text-decoration-line: line-through;
      text-decoration-thickness: initial;
      text-decoration-style: dashed/dotted/solid/wavy;
      text-decoration-color: red;
      ```
  - `text-shadow` `box-shadow`
    - （水平偏移 垂直偏移 模糊半径 颜色, 下一组）;
  - `white-space`如何处理元素中的空格
    - `normal` 连续的空白符会被合并，换行符会被当作空白符来处理。
    - `nowrap` 和 `normal` 一样，连续的空白符会被合并。但文本内的换行无效。
    - `pre` 连续的空白符会被保留。在遇到换行符或者 `<br>` 元素时才会换行。
    - `pre-wrap` 连续的空白符会被保留。在遇到换行符或者`<br>`元素，或者需要为了填充「行框盒子 (line boxes)」时才会换行。
    - `pre-line` 连续的空白符会被合并。在遇到换行符或者`<br>`元素，或者需要为了填充「行框盒子 (line boxes)」时会换行。
    - `break-spaces` 与 `pre-wrap` 的行为相同，除了：
      - 任何保留的空白序列总是占用空间，包括在行尾。
      - 每个保留的空格字符后都存在换行机会，包括空格字符之间。
      - 这样保留的空间占用空间而不会挂起，从而影响盒子的固有尺寸（最小内容大小和最大内容大小）。
  - `word-break` 指定了怎样在单词内断行
    - `normal` 使用默认的断行规则。
    - `break-all` 对于 non-CJK 文本，可在任意字符间断行。
    - `keep-all` CJK 文本不断行。Non-CJK 文本表现同 normal。
  - `overflow-wrap` 当一个不能被分开的字符串太长而不能填充其包裹盒时，为防止其溢出，浏览器是否允许这样的单词中断换行
    - `normal` 行只能在正常的单词断点处中断。（例如两个单词之间的空格）。
    - `break-word` 表示如果行内没有多余的地方容纳该单词到结尾，则那些正常的不能被分割的单词会被强制分割换行。
# 7-11
## 元素框
- 从外到内：
  - margin
  - border
  - padding
  - content
- width 和 height 的定义
  - content box 的宽度和高度
## 水平格式化
- 正常流中块级元素框的水平部分总和等于父元素的内容区宽度：
  - 父元素 content box width 等于以下相加：
  - `margin-left` 可以设为 auto
  + `border-left` 必须设定值，默认为 0
  + `padding-left` 必须设定值，默认为 0
  + `width` 可以设为 auto
  + `padding-right` 必须设定值，默认为 0
  + `border-right` 必须设定值，默认为 0
  + `margin-right` 可以设为 auto
- 当格式化属性过分受限时，总会把 `margin-right` 设为 `auto`
- ```css
  {
    <!-- 元素居中 -->
    width: 100px;
    margin: auto;
  }
  ```
# 7-12
## 垂直格式化
- `margin-top` 和 `margin-bottom` 设置为 auto 会自动计算 为 0
- 即不可以设置垂直居中
- 垂直方向的 margin 和 padding 的百分比值基于包含块的宽度计算
- margin 合并
  - 父元素块若没有 border 或 padding，字元素最上和最下方的 margin 会合并
- 合并时保留绝对值较大者
- BFC
  - Block Formatting Context 块级格式化上下文
  - 加边框不能触发BFC
  - 功能之一是阻止 margin 跑到父元素之外；但不能阻止兄弟元素之间 margin 合并
  - 如何触发：
    - `display: flow-root;`
    - `overflow: auto/hidden;`
- 负数 margin
  - 不叠加，取绝对值较大者
- 正负数 margin
  - 相互抵消
- BFC 包裹字元素的所有 margin-box
  - 无BFC 包裹字元素的 border-box
