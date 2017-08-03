---
layout: post
title:  "Mac下通过jekyll维护自己的GitHub pages"
date:   2017-08-03 15:04:01 +0800
categories: jekyll
tag: jekyll
---

* content
{:toc}

> 种一棵树最好的时间是十年前，其次是现在。

历经两天的时间终于弄好了我的github博客。

这也是我在自己博客上发布的第一篇文章，好兴奋！好激动！加油！

不知道怎么，开始学习swift语言，学着学着就对GitHub pages感兴趣了，从昨天研究到现在，历经重重艰难，终于是弄好了。

但我坚信建立一个属于自己的博客，是未来学习进步必不可少的前提条件，以后可以通过自己的这个博客记录一些自己的想法。

总结一下这两天的收获吧！

# 引擎和theme的选择
通过网络查资料，我决定使用jekyll构建自己的github pages，这样以后可以更好的迁移。

浏览了很多jekyll themes，最后选择了这个，是一个Java编程大大改编的，感觉简洁，好看。

在此感谢作者[Freud Kang](http://www.hifreud.com)大大！

# jekyll theme的使用
jekyll theme使用很简单，到网上搜索有很多，找到自己喜欢的theme后fork，在自己GitHub-profile-settings中修改name为(自己的用户名).github.io自己的博客也就有了。

# jekyll的安装
我用的2011年的MacBook Pro，系统是OS X EI Capitan Version 10.11.6 配置不是很高，一般而已。
自带Ruby，但是版本较低，开始不知道需要先更新Ruby，结果走了很多弯路。

安装jekyll可真是把我难住了，各种出错，各种失败，通过无数次的查资料和摸索最后终于安装成功了。总结如下：
1. 先通过终端查看当前rvm版本 `$ rvm -v` 确认机器已装有rvm
2. 查看当前ruby版本 `$ ruby -v` 确认机器已装有Ruby
3. 查看ruby所有版本 `$ rvm list known`
4. 安装最新版本ruby `$ rvm install 2.4`
5. 更新gem `$ gem update -system`
6. gem更新后可直接安装jekyll `$ gem install jekyll`
7. 在安装最新版本的Ruby前，千万不要用什么网上说的"使用国内的淘宝镜像"什么的，否则会出现无数的错误，我就在这浪费了大量时间
   > 安装jekyll前不要添加 `$ gem sources -a https://gems.ruby-china.org/`
8. 我现在也没有使用什么国内的gem，没有任何问题
9. 安装jekyll时如果提示：
   ```
   ERROR:  While executing gem ... (Errno::EPERM)
   Operation not permitted - /usr/bin/sass
   ```
   可以指定安装路径即可 `$ sudo gem install jekyll -n /Users/***/Documents/jekyll`
10. sudo是个很有用的命令，很多时候会提示没有权限的错误，带`write`的错误，可以使用sudo这个命令，输入mac的密码就可以了。

> 我们可以在自己的GitHub中在线直接修改页面内容，但是有时候这样比较麻烦，想实时修改查看自己的博客就需要构建本地的GitHub pages，这就需要使用到前面的jekyll了。

# 维护本地GitHub pages
通过这两天的研究，我总结了要想维护本地的GitHub pages必须要有以下三样工具：
* 本地安装jekyll
* 本地安装GitHub Desktop
* 本地的前端编辑器 *我使用了webstrom*

我的步骤是这样的：
1. 先本地安装好jekyll（前面已经讲过了）
2. 安装[GitHub Desktop](https://central.github.com/deployments/desktop/desktop/latest/darwin)，登陆自己的GitHub账号，clone自己刚才在GitHub上创建好的project
3. 安装webstorm，打开clone好的文件夹，一般在自己电脑的Documents/GitHub/***.github.io文件夹，然后就可以修改自己的网站内容了。
4. 进入终端，使用`$ cd`命令进入Documents/GitHub/***.github.io文件夹中，然后使用命令 `$ jekyll server` 运行jekyll，进入浏览器使用页面[localhost:4000](http://localhost:4000)通过刷新随时查看自己对网站的改动。
5. 进入GitHub Desktop可以查看到所有对网站的修改内容，提交修改内容，点击"etch origin"将修改内容同步到GitHub中，这样就完成了自己网站的维护操作。


在浏览器中输入自己的博客地址，欣赏自己美丽的博客吧！！！
> 种一棵树最好的时间是十年前，其次是现在。



[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
