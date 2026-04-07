---
title: "hexo加github搭建博客网站"
date: 2026-03-19
coverImage: "屏幕截图-2026-03-21-180633.png"
---

**环境准备**

**下载[node.js](http://\(https://nodejs.org/en/\))(**https://nodejs.org/en/**)**

**下载[git](https://git-scm.com/downloads)(**https://git-scm.com/downloads**)**

**验证下载（cmd中运行）**

node -v

npm -v（这个是node附带的）

git -v

![](https://suyihang15.com/wp-content/uploads/2026/03/屏幕截图-2026-03-21-180633-1024x539.png)

**下载hexo**

npm install hexo-cli -g

**搭建github仓库**

注册并登录[github](https://github.com/)（github用于托管我们的文件）

点击Create a new repository（创建仓库）

用户名.github.io

勾选 Public

勾选 Add a README file

拉到下面点击create创建

**生成SSH Keys**

在Git bash here输入

ssh-keygen -t rsa -C "邮件地址"四下回车

找C:\\Users\\用户名\\.ssh\\id\_rsa.pub复制

**github创建ssh**

设置里面找ssh keys

复制粘贴创建

**验正**

git中输入ssh -T git@github.com后yes

**本地搭建**

新建文件夹

git中输入

hexo init

hexo install

hexo g

hexo s

如果不行就加npx

**改配置文件**

打开\_config.yml

拉到最下面将deploy后面的全删掉，复制粘贴这段

  deploy:

  type: git

  repository: git@github.com:名字/名字.github.io.git

  branch: main

  注意格式

**安装自动部署发布工具**

npm install hexo-deployer-git --save  

然后在Blog文件夹右键打开git bash，依次输入

hexo g（生成）

hexo d（上传）

**第一次使用git的话会需要配置**

git config --global user.email "你的邮箱"

git config --global user.name "你的名字"

配置完后再hexo d上传

在跳出来的窗口内进行登录

接下来我们就成功把本地内容上传到github了

上传成功以后，我们就算搭建好了！上自己的网址看看吧

**网址是我们之前设的仓库名：**

用户名.github.io

**用记事本打开我们新建文件夹中的\_config.yml文件**

将Site下面按自己的需求填上

**Site**

title: 标题

subtitle: 副标题

description: 描述

keywords: 关键词

author: 站主

language: 语言（可以填写zh-CN）

timezone: 时区（可以填写Asia/Shanghai）

然后保存

**上传文章**

我们在新建文件夹中打开git bash,

输入下方代码就可以生成新的文章md文件

hexo new 文章标题

**注意**

文章是.md格式，在我们的Blog文件夹中的source/\_posts中

\_config.yml是配置文件自己修改就行

查看成果（这是本人搭建的成果）

[Mr.苏的博客https://suyihang15.github.io/](https://suyihang15.github.io/)

![](https://suyihang15.com/wp-content/uploads/2026/03/屏幕截图-2026-03-21-180448-1024x461.png)
