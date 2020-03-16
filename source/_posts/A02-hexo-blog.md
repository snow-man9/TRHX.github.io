---
title: 使用 Github Pages 和 Hexo 搭建自己的独立博客
categories: Hexo
tags:
 - Github Pages
 - Hexo
music:
  enable: true
  autoplay: true
  server: netease
  type: song
  id: 441552
thumbnail: https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/thumbnail/hexo.png
avatar: https://cdn.jsdelivr.net/gh/TRHX/CDN-for-itrhx.com@2.1.9/images/trhx.png
icons: [fas fa-heading]
---

![01](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/01.png)

<!-- more -->

# <font color=#FF000>-- 前言</font>
> 首先感谢您能访问我的博客：[TRHX'S BLOG](https://trhx.github.io)

这是一篇有关如何使用 <font color=#DC143C>Github Pages</font> 和 <font color=#DC143C>Hexo</font> 搭建属于自己独立博客的详尽教程，本人是软件工程专业本科生，目前只学习了C和C++编程语言，对网站开发的有关知识几乎为零，这也是我搭建好自己的博客之后写的第一篇博客，刚开始搭建博客的时候自己也是网上各种百度，由于自己属于<font color=#DC143C>小白</font>那种，历经了千辛万苦才弄好，所以借这个机会写一篇小白真正能看懂的博客搭建教程，教你一步一步走向成功的彼岸！

推荐文章： [《我为什么写博客》](http://www.cnblogs.com/jhzhu/p/3893297.html) （By 知明所以）  
　　　　 　[《为什么你应该（从现在开始就）写博客》](http://mindhacks.cn/2009/02/15/why-you-should-start-blogging-now/)  (By 刘未鹏 | Mind Hacks)

# <font color=#FF000>-- 入门</font>

> **Github Pages**

Github Pages可以被认为是用户编写的、托管在github上的静态网页。使用Github Pages可以为你提供一个免费的服务器，免去了自己搭建服务器和写数据库的麻烦。此外还可以绑定自己的域名。

> **Hexo**

Hexo 是一个快速、简洁且高效的博客框架。Hexo 使用 Markdown（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。

# <font color=#FF000>-- 安装 Node.js</font>
[点击此处](https://nodejs.org/en/download/)访问官网，按需下载相应版本，默认安装可以了

![02](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/02.jpg)

注：本人在安装过程中出现了Warning 1909,无法创建快捷方式，这种情况很少出现，如果在安装过程中也有这种情况请参考百度文库（win10系统实测可行）：[《Win7安装程序警告1909无法创建快捷方式》](https://wenku.baidu.com/view/4ad59110964bcf84b9d57ba5.html)

![03](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/03.jpg)

# <font color=#FF000>-- 安装 Git</font>
[点击此处](https://git-scm.com/download/win)访问官网，按需下载相应版本，默认安装即可
参考资料：[《如何在windows下安装GIT》](https://www.cnblogs.com/jytx/p/5602927.html) 　（By 俊雨廷休）  
　　　　　[《Pro Git（中文版）》](http://git.oschina.net/progit/)

# <font color=#FF000>-- 检验软件是否安装成功</font>
同时按下 Win 键和 R 键打开运行窗口,输入 <font color=#DC143C>cmd</font> ，然后输入以下命令，有相应版本信息显示则安装成功，若不正确可以卸载软件重新安装，此外若安装成功，在桌面右键鼠标，可以看到菜单里多了 <font color=#DC143C>Git GUI Here</font> 和 <font color=#DC143C>Git Bash Here</font>两个选项，第一个是<font color=#DC143C>图形界面的Git操作</font>，另一个是<font color=#DC143C>命令行</font> 
``` 
$ git --version
$ node -v
$ npm -v
```
![04](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/04.jpg)

![05](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/05.jpg)


# <font color=#FF000>-- Hexo 安装</font>
选择一个磁盘，新建一个文件夹，自己重命名文件夹（如：我的文件夹为：<font color=#DC143C>Ｅ\TRHX_Blog</font>），博客相关文件将储存在此文件夹下，在该文件夹下右键鼠标，点击 <font color=#DC143C>Git Bash Here</font>，输入以下 npm 命令即可安装，第一个命令表示安装 hexo，第二个命令表示安装 hexo 部署到 git page 的 deployer，如图所示即为安装成功  
```
$ npm install hexo-cli -g
$ npm install hexo-deployer-git --save
```
![06](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/06.png)

# <font color=#FF000>-- Hexo 初始化配置</font>
在刚才新建的文件夹里面再次新建一个 <font color=#DC143C>Hexo</font> 文件夹（如：我的文件夹为：<font color=#DC143C>E\TRHX_Blog\Hexo</font>）,进入该 <font color=#DC143C>Hexo</font> 文件夹右键鼠标，点击 <font color=#DC143C>Git Bash Here</font>，输入以下命令，如图所示则安装成功
```
$ hexo init
```
![07](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/07.png)

Hexo 安装完成后，将会在指定文件夹中新建所需要的文件，Hexo 文件夹下的目录如下：
![08](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/08.jpg)

# <font color=#FF000>-- 本地查看效果</font>
执行以下命令，执行完即可登录 [http://localhost:4000/](http://localhost:4000/) 查看效果
```
$ hexo generate
$ hexo server
```
显示以下信息说明操作成功：
```
INFO Hexo is running at http://0.0.0.0:4000/. Press Ctrl+C to stop.
```
登录 [http://localhost:4000/](http://localhost:4000/) 查看效果：
![09](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/09.jpg)

# <font color=#FF000>-- 将博客部署到 Github Pages 上</font>
到目前为止，我们的本地博客就成功搭建了，但是现在我们只能通过本地连接查看博客，我们要做的是让其他人也能够访问我们的博客，这就需要我们将博客部署到Github Pages上

一、注册 Github 账户：[点击此处](https://github.com)访问 Github 官网，点击 Sign Up 注册账户

二、创建项目代码库：点击 <font color=#DC143C>New repository</font> 开始创建，步骤及注意事项见图：
![10](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/10.jpg)

三、配置 <font color=#DC143C>SSH</font> 密钥：只有配置好 <font color=#DC143C>SSH</font> 密钥后，我们才可以通过 git 操作实现本地代码库与 Github 代码库同步，在你第一次新建的文件夹里面（如：我的文件夹为：<font color=#DC143C>Ｅ\TRHX_Blog</font>） <font color=#DC143C>Git Bash Here</font> 输入以下命令：  
```
$ ssh-keygen -t rsa -C "your email@example.com"
//引号里面填写你的邮箱地址，比如我的是tanrenhou@126.com
```
之后会出现： 
```
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/you/.ssh/id_rsa):
//到这里可以直接回车将密钥按默认文件进行存储
```
然后会出现：
```
Enter passphrase (empty for no passphrase):
//这里是要你输入密码，其实不需要输什么密码，直接回车就行
Enter same passphrase again:
```
接下来屏幕会显示：  
```
Your identification has been saved in /c/Users/you/.ssh/id_rsa.
Your public key has been saved in /c/Users/you/.ssh/id_rsa.pub.
The key fingerprint is:
这里是各种字母数字组成的字符串，结尾是你的邮箱
The key's randomart image is:
这里也是各种字母数字符号组成的字符串
```
运行以下命令，将公钥的内容复制到系统粘贴板上
```
$ clip < ~/.ssh/id_rsa.pub
```
四、在 GitHub 账户中添加你的公钥

1.登陆 GitHub，进入 <font color=#DC143C>Settings</font>：
![11](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/11.jpg)

2.点击 <font color=#DC143C>SSH and GPG Keys</font>：
![12](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/12.jpg)

3.选择 <font color=#DC143C>New SSH key</font>：
![13](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/13.jpg)

4.粘贴密钥：
![14](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/14.jpg)

五、测试

输入以下命令：<font color=#DC143C>注意：git@github.com不要做任何更改！</font>
```
     $ ssh -T git@github.com
```
之后会显示：
![15](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/15.png)

输入 <font color=#DC143C>yes</font> 后会显示：
![16](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/16.png)
此时表示设置正确

六、配置 Git 个人信息

Git 会根据用户的名字和邮箱来记录提交，GitHub 也是用这些信息来做权限的处理，输入以下命令进行个人信息的设置，把名称和邮箱替换成你自己的，名字可以不是 GitHub 的昵称，但为了方便记忆，建议与 GitHub  一致
```
     $ git config --global user.name "此处填你的用户名"
     $ git config --global user.email "此处填你的邮箱"
```
到此为止 SSH Key 配置成功，本机已成功连接到 Github

# <font color=#FF000>-- 将本地的 Hexo 文件更新到 Github 的库中</font>
一、登录 Github 打开自己的项目 <font color=#DC143C>yourname.github.io</font>
![17](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/17.jpg)

二、鼠标移到 <font color=#DC143C>Clone or download</font> 按钮，选择 <font color=#DC143C>Use SSH</font>
![18](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/18.jpg)

三、一键复制地址
![19](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/19.jpg)

四、打开你创建的 <font color=#DC143C>Hexo</font> 文件夹（如：<font color=#DC143C>E:\TRHX_Blog\Hexo</font>），右键用记事本（或者Notepad++、Vs Code等）打开该文件夹下的 <font color=#DC143C>_config.yml</font> 文件
![20](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/20.jpg)

五、按下图修改 <font color=#DC143C>_config.yml</font> 文件并保存
![21](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/21.png)

六、在 <font color=#DC143C>Hexo</font> 文件夹下分别执行以下命令
```
     $ hexo g
     $ hexo d
```
或者直接执行
```
     $ hexo g -d
```
执行完之后会让你输入你的 Github 的账号和密码，如果此时报以下错误，说明你的 deployer 没有安装成功
```
     ERROR Deployer not found: git
```
需要执行以下命令再安装一次：
```
     npm install hexo-deployer-git --save
```
再执行 <font color=#DC143C>`hexo g -d`</font>，你的博客就会部署到 Github 上了

七、访问博客

你的博客地址：<font color=#DC143C>https://你的用户名.github.io</font>，比如我的是：<font color=#DC143C>https://trhx.github.io</font> ，现在每个人都可以通过此链接访问你的博客了

# <font color=#FF000>-- 如何在博客上发表文章</font>

博客已经成功搭建了，但是我们该怎么写博客呢？

一、新建一个空文章，输入以下命令，会在项目 <font color=#DC143C>\Hexo\source\\_posts</font> 中生成 <font color=#DC143C>文章标题.md</font> 文件，文章标题根据需要命名
```
     $ hexo n "文章标题"
```
也可以直接在 <font color=#DC143C>\Hexo\source\\_posts</font> 目录下右键鼠标新建文本文档，改后缀为 <font color=#DC143C>.md</font> 即可，这种方法比较方便

二、用编辑器编写文章

<font color=#DC143C>md</font> 全称 Markdown， Markdown 是 2004 年由 John Gruberis 设计和开发的纯文本格式的语法，非常的简单实用，常用的标记符号屈指可数，几分钟即可学会， <font color=#DC143C>.md</font> 文件可以使用支持 Markdown 语法的编辑器编辑，然后将写好的文章（.md文件）保存到 <font color=#DC143C>\Hexo\source\\_posts</font> 文件夹下即可

推荐 Windows 上使用 <font color=#DC143C>MarkdownPad2</font> 或者 <font color=#DC143C>小书匠</font> 编辑器，macOS 上使用 <font color=#DC143C>Mou</font> 编辑器，Linux 上使用 <font color=#DC143C>Remarkable</font> 编辑器，Web 端上使用<font color=#DC143C> 简书</font> ，另外可以参考我的另一篇文章：[《主流 Markdown 编辑器推荐》](https://www.itrhx.com/2018/08/29/A05-Markdown-editor-recommendation/)
当我们用编辑器写好文章后，可以使用以下命令将其推送到服务器上
```
     $ hexo g
     $ hexo d
```
或者将两个命令合二为一输入以下命令：
```
     $ hexo d -g
```
现在访问你的博客就可以看见写好的文章啦！
参考资料：[《10款流行的Markdown编辑器》](https://blog.csdn.net/jinhui157/article/details/73872795) （By xiaoxiao_engineer）  
　　　　　[《献给写作者的 Markdown 新手指南》](https://www.jianshu.com/p/q81RER/) （By 简书）
　　　　　[《认识与入门 Markdown》](https://sspai.com/post/25137) （By Te_Lee）
　　　　　[《markdown简明语法》](http://ibruce.info/2013/11/26/markdown/) （By 不如）
　　　　　[《markdown基本语法》](https://www.jianshu.com/p/191d1e21f7ed) （By 高鸿祥）
　　　　　[《Markdown 公式指导手册》](http://www.liuhaihua.cn/archives/143443.html) （By Harries）  


# <font color=#FF000>-- 如何为博客更换自己喜欢的主题</font>

博客也搭建好了，文章也会写了，但是！！！默认的主题并不喜欢怎么办？现在，我们就来为自己的博客更换自己喜欢的主题

[点击此处](https://hexo.io/themes/)进入 Hexo 官网的主题专栏，我们可以看见有许多的主题供我们选择
![22](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/22.jpg)

我们要做的就是把主题克隆过来，在此我们以主题 <font color=#DC143C>Aero-Dual</font> 为例，点进去我们就可以看见该主题作者的博客，鼠标滑到底，我们可以看见 <font color=#DC143C>Theme By Levblanc</font> 的字样（其他主题类似），点击作者 <font color=#DC143C>Levblanc</font> ，页面就会跳转到该主题所有的相关文件在 Github 上的地址，复制该地址
![23](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/23.png)
![24](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/24.jpg)
![25](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/25.jpg)

再打开 <font color=#DC143C>Hexo</font> 文件夹下的 <font color=#DC143C>themes</font> 目录（如：<font color=#DC143C>E:\TRHX_Blog\Hexo\themes</font>），右键 <font color=#DC143C>Git Bash Here</font>，输入以下命令：
```
     $ git clone 此处填写你刚才复制的主题地址
```
比如要安装 <font color=#DC143C>Aero-Dual</font> 主题，则输入命令：
```
     $ git clone https://github.com/levblanc/hexo-theme-aero-dual
```
等待下载完成后即可在 <font color=#DC143C>themes</font> 目录下生成 <font color=#DC143C>hexo-theme-aero-dual</font> 文件夹，然后打开 <font color=#DC143C>Hexo</font> 文件夹下的配置文件 <font color=#DC143C>_config.yml</font> ，找到关键字 <font color=#DC143C>theme</font>，修改参数为：<font color=#DC143C>theme：hexo-theme-aero-dual</font> （其他主题修改成相应名称即可），再次注意冒号后面有一个空格！
![26](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/26.jpg)

返回 <font color=#DC143C>Hexo</font> 目录，右键 <font color=#DC143C>Git Bash Here</font> ，输入以下命令开始部署主题：
```
     $ hexo g   
     $ hexo s
```
此时打开浏览器，访问 [http://localhost:4000/](http://localhost:4000/)  就可看见我们的主题已经更换了，如果感觉效果满意，我们就可以把它部署到Github上了

打开 <font color=#DC143C>Hexo</font> 文件夹，右键 <font color=#DC143C>Git Bash Here</font> ，输入以下命令：
```
     $ hexo clean  
     //该命令的作用是清除缓存，若不输入此命令，服务器有可能更新不了主题
     $ hexo g -d
```
此时访问自己的博客即可看见更换后的主题，但我们仍然需要对主题的相关配置进行修改，比如网站标题，图标等等，Hexo 中有两份主要的配置文件，名称都是  <font color=#DC143C>_config.yml</font> ，它们均是用于站点配置使用的。其中，一份位于站点根目录下（比如我的：<font color=#DC143C>E:\TRHX_Blog\Hexo\\_config.yml</font>），主要包含 Hexo 本身整站的配置；另一份位于主题目录下（比如我的：<font color=#DC143C>E:\TRHX_Blog\Hexo\themes\hexo-theme-aero-dual\\_config.yml</font>），这份配置由主题作者提供，主要用于配置主题相关的选项，一般  <font color=#DC143C>_config.yml</font>  文件里都有相关注释，按需修改即可

参考资料：[《有哪些好看的 Hexo 主题？》](https://www.zhihu.com/question/24422335) （知乎）  
　　　　　[《Hexo | 配置》](https://hexo.io/zh-cn/docs/configuration.html) （Hexo官方文档）  
　　　　　[《hexo常用命令笔记》](https://segmentfault.com/a/1190000002632530) （By 小弟调调）

# <font color=#FF000>-- 为你的 Hexo 博客配置个性域名</font>

本人在配置域名的时候问题百出，百度的各种方法都不管用，打开网站总是 404，可能是我太笨了 　o(╥﹏╥)o　，不过好在后来终于解决了这个问题

首先我们要购买域名，[阿里云](https://www.aliyun.com)，[腾讯云](https://cloud.tencent.com)都可以，也不贵，一年几十块钱，最便宜几块钱也能买到，以阿里云为例，我购买的域名是 [itrhx.com](https://www.itrhx.com)，购买过程就不赘述了，选择阿里云的解析平台，来到阿里云的管理控制台，点击进入域名解析列表或者直接点击域名后面的解析
![27](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/27.jpg)

方法一：点击添加记录，需要添加两个记录，两个记录类型都是 <font color=#DC143C>CNAME</font> ，第一个主机记录为 <font color=#DC143C>@</font> ，第二个主机记录为 <font color=#DC143C>www</font>，记录值都是填你自己的博客地址（比如我的是：<font color=#DC143C>[trhx.github.io](http://trhx.github.io)</font>），保存之后域名解析就完成了！
![28](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/28.jpg)
方法二：两个记录类型为 <font color=#DC143C>A</font> ，第一个主机记录为 <font color=#DC143C>@</font> ，第二个主机记录为 <font color=#DC143C>www</font>，记录值都为博客的 <font color=#DC143C>IP</font> 地址，<font color=#DC143C>IP</font> 地址可以 <font color=#DC143C>cmd</font> 中输入 <font color=#DC143C>ping 你的博客地址</font> 获得（比如我的：<font color=#DC143C>ping trhx.github.io</font>），保存之后域名解析就完成了！
![](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/29.jpg)
有关解析记录类型的区别可以参考[《域名解析中A记录、CNAME、MX记录、NS记录的区别和联系》](https://blog.csdn.net/it_man/article/details/9017307) 

为了使 GitHub 接收我们的域名，还需要在博客的根目录下添加一个名为 <font color=#DC143C>CNAME</font> 的文件（<font color=#DC143C>注意不要加.txt，没有任何后缀名！</font>），这个文件放到 <font color=#DC143C>Hexo</font> 文件夹的 <font color=#DC143C>source</font> 里面，（比如我的是：<font color=#DC143C>E:\TRHX_Blog\Hexo\source</font>），文件里面填写你的域名（<font color=#DC143C>加不加www都行</font>），比如要填写我的域名，文件里面就写：<font color=#DC143C>www.itrhx.com</font> 或者 <font color=#DC143C>itrhx.com</font>，经过以上操作，别人就可以通过 [www.itrhx.com](http://www.itrhx.com) 、[itrhx.com](https://itrhx.com) 、[trhx.github.io](https://trhx.github.io) 三个当中任意一个访问我的博客了！你的也一样！

有关加不加www的问题有以下区别：
> 如果你填写的是没有www的，比如 itrhx.com，那么无论是访问 https://www.itrhx.com 还是 https://itrhx.com ，都会自动跳转到 https://itrhx.com

> 如果你填写的是带www的，比如 www.itrhx.com ，那么无论是访问 https://www.itrhx.com 还是 https://itrhx.com ，都会自动跳转到 http://www.itrhx.com


![30](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A02/30.jpg)

如果你在其他平台购买域名，或者选择 [DNSPod](https://www.dnspod.cn) 等其他域名解析，操作方法大同小异，遇到问题可自行百度解决！

参考资料：[《推荐几家域名注册服务商》](https://zhuanlan.zhihu.com/p/27349039)  （By Jelly Bool）  
　　　　　[《盘点十大免费DNS域名解析服务：稳定、可靠》](http://www.chinaz.com/web/2015/0122/380042.shtml)

# <font color=#FF000>-- 结语</font>
一顿操作下来虽然有点儿累，但看见拥有了自己的博客还是非常有成就感的，人生就是需要折腾，那么现在就开始你的创作之旅吧！文章的不断积累，你会从中受益很多的！另外，这是一篇小白写的适用于小白的博客搭建教程，比较详细，有这方面基础的可以百度有简略一点儿的教程，文中如有错误还请大佬指出改正！文中涉及参考资料如有侵权请联系我删除！