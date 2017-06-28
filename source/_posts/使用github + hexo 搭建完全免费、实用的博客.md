---
title: 使用github+hexo 搭建完全免费、实用的博客
date: 2017-04-18 20:48:33
categories: experience
tags: ['新手经历', '博客搭建', 'HeXo']
keywords: Hexo, Blog
---
> 断剑重铸之日，骑士归来之时！   --- 向着自由，向着未来出发Aco (๑╹◡╹)ﾉ"""

---
我的第一篇博客
==========================
[TOC]
## 1，搭建环境准备
> - Node.js 的安装和准备 
- Git的安装和准备 
- gitHub账户的配置

<!-- more -->

### 1.1 配置Node.js环境
>   1.1.1下载Node.js安装文件：去官网选择合适的版本安装 [Node.js官网](https://nodejs.org/en/download/)

<center>![](http://wx3.sinaimg.cn/mw690/006xRFa6gy1feqxnr2staj30iu0cz0tb.jpg)</center>

<center>![](http://wx2.sinaimg.cn/mw690/006xRFa6gy1fer60tojslj30dv0atwh7.jpg)</center>

具体安装教程网上都有，提供两个教程链接吧
[菜鸟教程Node.js 安装配置](http://www.runoob.com/nodejs/nodejs-install-setup.html)
[CSDN博客NodeJS、NPM安装配置步骤(windows版本)](http://blog.csdn.net/xxmeng2012/article/details/51492149)

具体安装过程这里就不赘述了，安装完成之后，需要检查一下是否安装成功，打开命令行窗口（Win+R，输入cmd回车）在打开的命令行界面中，输入
``` bash
node -v
npm -v
```
如果显示下图，则node.js安装完成，我们可以开始下一步了。
<center>![](http://wx4.sinaimg.cn/mw690/006xRFa6gy1feqxomc9y1j30g408fdft.jpg)</center>

### 1.2 Git的安装和准备
> 1.2.1 区官网下载Git安装文件,选择一个合适的版本：[Git Dowload](https://git-scm.com/downloads/)

<center>![](http://wx1.sinaimg.cn/mw690/006xRFa6gy1feqxo11pzrj30kd0bygny.jpg)</center>

<center>![](http://wx1.sinaimg.cn/mw690/006xRFa6gy1fer6cz5wy6j30e70b1gpo.jpg)</center>

安装过程同样自己找教程，这里提供一个[百度经验图文详解Windows下安装最新版Git](http://jingyan.baidu.com/article/020278117cbe921bcc9ce51c.html)
同样，也需要检查一下
``` bash
git --version
```
> 1.2.2 github账户的注册和配置

如果已经拥有账号，请跳过此步~如果没有，请接着看
> 1）Github注册
打开https://github.com/，在下图的框中，分别输入自己的用户名，邮箱，密码。
然后前往自己刚才填写的邮箱，点开Github发送给你的注册确认信，确认注册，结束注册流程。
一定要确认注册，否则无法使用gh-pages！
2）创建代码库
登陆之后，点击页面右上角的加号，选择New repository：
<center>![](http://wx2.sinaimg.cn/mw690/006xRFa6gy1feqxoh24w0j30iw0fgt9f.jpg)</center>
新建一个名为yourname.github.io的仓库，比如说，如果你的github用户名是test，那么你就新建test.github.io的仓库（必须是你的用户名，其它名称无效），将来你的网站访问地址就是 http://test.github.io 了，是不是很方便？

>>几个注意的地方：
  1. 注册的邮箱一定要验证，否则不会成功！
  2. 仓库名字必须是：username.github.io，其中username是你的用户名！

>3）代码库设置
开启GitHub Pages功能，点击界面右侧的Settings，你将会打开这个库的setting页面，向下拖动，直到看见GitHub Pages，点击Automatic page generator，Github将会自动替你创建出一个gh-pages的页面。
<centerr>![](http://wx4.sinaimg.cn/mw690/006xRFa6gy1feqxojj42rj30jf0abdge.jpg)</center>
然后访问一下 yourname.github.io 这个网址就可以了

**至此，git的安装和配置已经完成，我们进入下一部分~**

## 2，HeXo的安装和配置
### 2.1 hexo安装
> 在自己认为合适的地方创建一个文件夹，这里我以D:\github\HeXo 为例子讲解，创建完成后，在命令行的窗口进入到该目录
输入
``` bash
npm install hexo-cli -g
```

> 可能你会看到一个WARN，但是不用担心，这不会影响你的正常使用。然后输入
``` bash
npm install hexo --save
```
> 然后你会看到命令行窗口刷了一大堆白字，下面我们来看一看Hexo是不是已经安装好了。 在命令行中输入：
``` bash
hexo -v
```
> 如果你看到了如图文字，则说明已经安装成功了。
<center>![](http://wx4.sinaimg.cn/mw690/006xRFa6gy1feqxomc9y1j30g408fdft.jpg)</center>

### 2.2 hexo的相关配置
> 2.2.1 初始化Hexo

接着上面的操作，输入：
``` bash
hexo init
```
然后输入：
``` bash
npm install
```
之后npm将会自动安装你需要的组件，只需要等待npm操作即可。继续操作，同样是在命令行中，输入：
``` bash
hexo g
```
然后输入：
``` bash
hexo s
```
然后会提示：
INFO Hexo is running at http://0.0.0.0:4000/. Press Ctrl+C to stop.
在浏览器中打开http://localhost:4000/，你将会看到：
<center>![](http://wx1.sinaimg.cn/mw690/006xRFa6gy1fer60vak0vj311y0lctp6.jpg)</center>

最后，输入
``` bash
npm install hexo-deployer-git --save
```
安装一个`扩展来支持git命令`

到目前为止，Hexo在本地的配置已经全都结束了。下面会讲解怎样`将Hexo与github page` 联系起来

## 3, 将Hexo与github page 联系起来
### 3.1 配置git个人信息 
如果你之前已经配置好git个人信息，请跳过这一个步骤
> 3.1.1 设置Git的user name和email：(如果是第一次的话)

输入注册时的用户名和邮箱
``` bash
git config --global user.name "yourname"
git config --global user.email "你注册时的邮箱@xx.com"
```
> 3.1.2 生成密钥

首先输入
``` bash
cd ~/. ssh 
```
检查本机是否已存在的ssh密钥
如果提示：No such file or directory 说明你是第一次使用git。输入:
``` bash
ssh-keygen -t rsa -C "你注册时的邮箱@xx.com"
```
`然后会提示是否需要密码，这个可设可不设，设了麻烦，不设不安全，自己抉择~`
最终会生成一个文件在用户目录下,打开用户目录,比如我的是`C:\Users\热血绅士\\.ssh`，找到.ssh\id_rsa.pub文件，记事本打开并复制里面的内容，打开你的github主页，进入个人设置 -> SSH and GPG keys -> New SSH key：将刚复制的内容粘贴到key那里，title随便填，保存。
> 测试是否成功，输入这个指令（就是git@github.com,不用改）
``` bash 
ssh -T git@github.com 
```
> 注意：如果提示Are you sure you want to continue connecting (yes/no)?，输入yes，然后会看到：
>> Hi Change-TheWorld! You’ve successfully authenticated, but GitHub does not provide shell access.

> 看到这个信息说明SSH已配置成功！

### 3.2 配置Deployment
同样在_config.yml文件中，找到Deployment，然后按照如下修改：
``` bash
deploy:
  type: git
  repo: git@github.com:yourname/yourname.github.io.git
  branch: master
```
这样就可以了,我之前配置的时候就是在这里吃了亏...
我 repo 写的是`https://github.com/Change-TheWorld/Change-TheWorld.github.io.git` 结果博客上传过程中一直报错，下面我会介绍一下错误及解决办法

## 4，发布
新建一篇博客，执行下面的命令：
``` bash
hexo new post "MyFirstBlog"
```
这时候在我的 电脑的目录下 `D:\github\HeXo\source_posts` 将会看到 `MyFirstBlog.md` 文件
用MarDown编辑器打开就可以编辑文章了。文章编辑好之后，运行生成.
`部署命令： hexo g  生成静态文件  hexo d 发布`
``` bash
hexo g 
hexo d 
```
当然你也可以执行下面的命令，相当于上面两条命令的效果，在部署前先生成
``` bash
hexo d -g 
```
部署成功后访问 你的地址，[https://yourName.github.io](https://yourName.github.io),将可以看到生成的文章。

## 5，出现的错误及解决办法
### 5.1 错误一
>"ssh: connect to host github.com port 22: Connection timed out"错误

在连接github时，执行
```
ssh -T Git@github.com
```
 命令时，出现"ssh: connect to host github.com port 22: Connection timed out"
> 解决办法：
进入在`存放公钥私钥(id_rsa和id_rsa.pub)`的文件夹,比如我的就是`C:\Users\热血绅士\\.ssh`，新建`config文件，不需要后缀名`
<center>![](http://wx2.sinaimg.cn/mw690/006xRFa6gy1feqxop072bj30k406edfw.jpg)</center>

用notepad++ 打开输入以下内容：
```
Host github.com
User YourEmail@xx.com
Hostname ssh.github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/id_rsa
Port 443
```
user填入你注册时的邮箱，用户名也可以~
再次执行`ssh -T git@github.com`时，会出现提示如下，回车`yes`即可。
<center>![](http://wx1.sinaimg.cn/mw690/006xRFa6gy1fer60u78xvj30ht042780.jpg)</center>

### 5.2 错误二
> "failed to connect to github.com port 443: Timed out" 

>一开始我尝试着设置
```bash
git config --global http.proxy socks5://192.168.192.136:8080
```
然并卵;改端口，然并卵.....后来我才发现我自己配置Deployment的时候
repo写的是`https://github.com/Change-TheWorld/Change-TheWorld.github.io.git` 问题就出在这个地方,这是为什么呢？

> `git@github.com:yourname/yourname.github.io.git` 与 `https://github.com/Change-TheWorld/Change-TheWorld.github.io.git`有什么区别吗？

> 这里我提供一个github官方的文档解释[github官方的文档解释](https://help.github.com/articles/changing-a-remote-s-url/)
github默认的是SSH方式，这样更快速，相对的操作也会麻烦一点，按照上面的配置，可以实现两种之间的转换.比如当你clone 一些资源的时候
``` bash
git clone https://github.com/iissnan/hexo-theme-next themes/next
```
要改成
``` bash
git clone git@github.com:iissnan/hexo-theme-next themes/next
```

## 6，与域名进行绑定
### 6.1 首先，要申请一个域名，我的是在腾讯云上申请的，学生认证后免费试用一年的个人域名

申请到了之后，进行域名的解析
![](http://wx4.sinaimg.cn/mw690/006xRFa6gy1feqxnkks57j30v50axjs8.jpg)

如图第一行和第二行，就是将我的域名与github上的博客的主页相绑定，配置好之后，到github博客项目根目录新建一个名为CNAME的文件（无后缀），里面填写你的域名，加不加www看你自己喜好，因为经测试：
> ● 如果你填写的是没有www的，比如 mygit.me，那么无论是访问 http://www.mygit.me 还是 http://mygit.me ，都会自动跳转到 http://mygit.me
  ● 如果你填写的是带www的，比如 www.mygit.me ，那么无论是访问 http://www.mygit.me 还是 http://mygit.me ，都会自动跳转到 http://www.mygit.me
  ● 如果你填写的是其它子域名，比如 abc.mygit.me，那么访问 http://abc.mygit.me 没问题，但是访问 http://mygit.me ，不会自动跳转到 http://abc.mygit.me
另外说一句，在你绑定了新域名之后，原来的你的用户名.github.io并没有失效，而是会自动跳转到你的新域名。

## 7，常用命令集合
> hexo new "postName" #新建文章
hexo new page "pageName" #新建页面
hexo generate #生成静态页面至public目录
hexo server #开启预览访问端口（默认端口4000，'ctrl + c'关闭server）
hexo deploy #部署到GitHub
hexo help  # 查看帮助
hexo version  #查看Hexo的版本

缩写
> hexo n == hexo new
hexo g == hexo generate
hexo s == hexo server
hexo d == hexo deploy

组合命令：
> hexo s -g #生成并本地预览
hexo d -g #生成并上传

## 8，发挥你的想象，开始你的博客之旅吧！

***<font size=5>以上~这就是我的第一篇博客，希望能够帮到大家</font>***

