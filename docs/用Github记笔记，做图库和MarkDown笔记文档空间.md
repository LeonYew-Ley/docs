# 用Github记笔记，做图库和MarkDown笔记文档空间
> Written with [StackEdit中文版](https://stackedit.cn/).
> 作者：[LeonYew | 黎恩瑜](http://leonyew.fun)
> 日期：2024年1月7日

# 引言
**前排提示：可以不看**

请原谅我的思维很跳跃，我常常会因为做一个东西，但是缺其他东西，然后把注意力转到其他东西，跳了好几次再转回来，我暂且把这种现象叫做**高墙悖论**。这么折腾的过程也是我写这篇文章的原因：

需要做Unity的期末作业 --> 需要写文档 --> 需要记录一些灵感 --> MarkDown --> 需要一个博客存放 --> 搭建halo --> 需要Docker -->需要DockerCompose --> 配置DockerCompose --> halo需要设置主题的HTML语言为中文，否则浏览器会弹出翻译 --> 自己修改官方的主题包 --> halo自带的编辑器不好用 --> StackEdit --> 需要连接到我自己的Github --> 配置Github文档空间和Github图库

总之，绕了一大圈之后，我是终于完成了可以开始记录的我的开发日志，但其实这一切我完全可以单独新建一个实验文档以外的docx文档就可以了，没办法，**人生乐在折腾**。
# 一、使用StackEdit中文版写MarkDown
## 你不会MarkDown?
没事，你进入到StackEdit中之后，会有一份Welcome的文档，里面有StackEdit支持的各种语法，**不用记，忘记的时候查一下就行，熟能生巧**。
## 中文版 or 国际版？
这里我推荐你使用StackEdit中文版，为什么？见下表：
||StackEdit中文版|StackEdit|
|--|--|--|
|文档空间|✅**Gitea** <br>✅**Gitee** <br>✅GitHub <br>✅GitLab <br>✅Google Drive <br>✅CouchDB|✅GitHub <br>✅GitLab <br>✅Google Drive <br>✅CouchDB |
|图床支持|✅当前文档空间<br> ✅SM.MS <br> ✅自定义图床账号<br> ✅Gitea仓库<br> ✅GitHub仓库|✅Google Photos|
|网址|stackedit.cn|stackedit.io|
|其他|没有广告和bar弹窗|有赞助bar弹窗|
所以我建议你使用中文版，毕竟支持Gitee，毕竟哪天梯子倒了，还可以访问 *StackEdit 中文版* 和自己的 *笔记仓库* 。
## StackEdit的使用
接下来的教程，我默认你使用了 StackEdit 中文版。
打开 stackedit.cn 你会看到如下界面：
![输入图片说明](https://raw.githubusercontent.com/LeonYew-SWPU/FileTem/main/imgs/2024-01-07/6PaJoOKpDcEYOC03.png)

在说明一下StackEdit有什么用：
- 一款网页的MarkDown编辑器
- 不用登陆也可以写文档，SE默认用的是浏览器本地缓存，所以，不要随便清理浏览器缓存，也不要使用隐身模式！
- 可以连接到云端仓库，把文件同步上去，Ctrl+S就是Git操作中将本地更改Commit并Push到远端仓库

我们继续来，点击开始写作，你就会来到StackEdit的欢迎文档（Welcome File）
![输入图片说明](https://raw.githubusercontent.com/LeonYew-SWPU/FileTem/main/imgs/2024-01-07/q2Xhb5XeZmUPL5IL.png)

你可以点击下一步学习一下SE的基本操作，我就直接跳过了。点击左上角打开文件资源管理器，可以查看文件有哪些。接下来，我们将SE**链接到Github**，并且利用Github Repo为我们搭建**免费的图床**，而且使用一些方法让**国内也能快速浏览**！

# 二、StackEdit绑定Github
这里如果你不能访问Github，使用Gitee也是一样的，大同小异，本文使用Github作为演示，如果有任何问题可以在我的个人网站私信我。[点我前往：LeonYew](http://leonyew.fun)
## 1. 登录Github/Gitee账号
我们点击右上角SE的中文版logo -->使用GitHub登录
![输入图片说明](https://raw.githubusercontent.com/LeonYew-SWPU/FileTem/main/imgs/2024-01-07/kTRMXFuYi2raxeQv.png)
## 2. 新建文档Repo和图库Repo
登录账号以后，你也许会看到SE右侧会有新建文档空间，但是在这之前，我们需要去GitHub上先把文档和图片的仓库建立好：
### 新建文档Repo
来到[Github](https://github.com/)，点击左上角的“New”新建仓库
![输入图片说明](https://raw.githubusercontent.com/LeonYew-SWPU/FileTem/main/imgs/2024-01-07/vnDZDs6mYeoiek21.png)
接下来，你会看到新建页面，红色的仓库名称是必填的，其他黑色的自行配置，我在截图中配了中文注释
![输入图片说明](https://raw.githubusercontent.com/LeonYew-SWPU/FileTem/main/imgs/2024-01-07/mipRoAOlAIO5S4Xq.png)
Description下面的仓库类型忘注释了，Public：公开，Private：私有。私有仓库可以你自己设置查看权限，一般用于研发中的团队项目，且需要Github会员，所以我们**选择Public**即可。

仓库名称必须是英文且不能有空格或特殊字符，填错了Github会提示你修改的，我们随便去个名字：比如SENotes

创建完成后，你会来到你的仓库，由于没有勾选README file，所以目前没有文件，暂时不用管。

你可以随便上传一些东西，用来确定分支的名称。

按照文档Repo的方式，**再新建一个仓库：SEImgs**。
## 3. 在StackEdit中连接到Github文档空间
当我们建立好仓库，就可以回到SE中绑定了。
我们点击右上角SE的中文版logo --> 文档空间 --> 新增GitHub文档空间，按照下图提示填写：
![输入图片说明](https://raw.githubusercontent.com/LeonYew-SWPU/FileTem/main/imgs/2024-01-07/TlE1HalJ67fmMDmY.png)

点击“确认”，会跳转到Github授权认证，一路**点击绿色按钮**即可。
接下来，稍等片刻，有时候会因为网络问题而卡在StackEdit的logo页面，如果等待超时了，只需要刷新重新添加文档空间即可。
添加成功后，StackEdit左边会出现仓库的markdown文件目录，右边会多出一个Github文档空间，如下图：
![输入图片说明](https://raw.githubusercontent.com/LeonYew-SWPU/FileTem/main/imgs/2024-01-07/stiJj8ZAVVLrjisE.png)
到这里，就算是添加成功了，接下来我们添加图库。

## 4. 在StackEdit中连接到Github图库
### 配置图库
随便新建一个文件，在编辑器的上方，会有一个图片图标，我们点击它：
![输入图片说明](https://raw.githubusercontent.com/LeonYew-SWPU/FileTem/main/imgs/2024-01-07/FCCWXWq4ubOayKFr.png)
选择添加Github仓库
![输入图片说明](https://raw.githubusercontent.com/LeonYew-SWPU/FileTem/main/imgs/2024-01-07/XWAu1vZ1oS7MyNW0.png)
点击确认，
![输入图片说明](https://raw.githubusercontent.com/LeonYew-SWPU/FileTem/main/imgs/2024-01-07/9bFQi0gh0JqxIFe3.png)
会跳转到Github认证，也是一路**点击绿色按钮**同意即可，是为了给予SE Git 仓库的权限。
认证完成后，会跳转到如下页面：和添加文档仓库类似，填写仓库地址和分支即可。
![输入图片说明](https://raw.githubusercontent.com/LeonYew-SWPU/FileTem/main/imgs/2024-01-07/eMadoHmWIFOqsj0X.png)
### 添加图片的两种办法
配置完图库之后，我们来说下使用SE如何使用图片
#### A. 截图之后直接粘贴（前提是截图工具默认复制图片到剪贴板）
在SE中，配置好图库之后，可以直接在文档中粘贴图片，就和QQ、Word等富文本编辑器一样的用法。
SE会自动将你的图片上传到配置好的图库中，并获取地址粘贴到MarkDown文档中。演示如下：
![输入图片说明](https://raw.githubusercontent.com/LeonYew-SWPU/FileTem/main/imgs/2024-01-07/I6iRl9rg4ruvzqqP.gif)
#### B. 上传图片
点击编辑器上方的图片按钮 -->上传图片 --> 选择图片文件，演示效果如下：
![输入图片说明](https://raw.githubusercontent.com/LeonYew-SWPU/FileTem/main/imgs/2024-01-07/f5SUFXBGFglw52ck.gif)

# 四、Github图库访问加速
你可能注意到了SE自动生成的图片地址为 raw.githubusercontent.com ，要是在国内的博客访问速度很慢怎么办？
这里分享一个方法：将github地址替换为jsdelivr的CDN服务商地址
>原文章：https://article.itxueyuan.com/oJWvvo

## 利用jsdelivr加速访问
1. 假设我们的仓库中有一张test.png的图片，使用github的链接直接访问是这样访问的`https://github.com/github用户名/仓库名/raw/master/test.png`
2. 转换为以下格式：`https://cdn.jsdelivr.net/gh/<你的github用户名>/<你的图床仓库名>@<仓库分支>/图片的路径` 

## 示例
|Github地址|CDN加速地址|
|--|--|
|https://raw.githubusercontent.com/LeonYew-SWPU/FileTem/main/imgs/2024-01-07/f5SUFXBGFglw52ck.gif|  https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024-01-07/f5SUFXBGFglw52ck.gif |
|![Github地址](https://raw.githubusercontent.com/LeonYew-SWPU/FileTem/main/imgs/2024-01-07/f5SUFXBGFglw52ck.gif)|![CDN加速地址](https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024-01-07/f5SUFXBGFglw52ck.gif )|

不过，对于以后如何自动让SE防止加速后的链接，我还没有比较好的方法。

不过或许可以通过去Github上 Fork SE中文版 的仓库，来修改一下它的图片处理逻辑，让它上传好仓库之后，粘贴回来的函数中增加一个转换链接的函数，让最终的路径为CDN加速路径。
# 五、GitHub与Gitee双向同步
这里展开说操作的话篇幅太大，所以请等待我写一篇新的文章并把链接附在这里。

# 结语
虽然说兜兜转转写博客又浪费了不少在期末项目上的时间，不过算是为之后的作业记录和开发日志“搭好了框架”。

最后，欢迎在评论区一起探讨~

> 《用Github记笔记，做图库和MarkDown笔记文档空间》
> Written with [StackEdit中文版](https://stackedit.cn/).
> 作者：[LeonYew | 黎恩瑜](https://github.com/LeonYew-Ley)
> 日期：2024年1月7日
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTUyODYxOTA5NCwtNzE1Mzc0OTg3XX0=
-->