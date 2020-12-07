---
layout: post
title:  "『学习笔记02』用github和jekyll和git来搭建自己的博客"
date:   2020-12-06
author: “Alte-yyk”
---



# 『学习笔记02』用github和jekyll和git来搭建自己的博客

*用这篇博客来记录自己如何从0到1搭建自己的简易博客，本人系统：unbuntu。*
## jekyll

Jekyll 是一个简单的博客形态的静态站点生产机器。官方定义？我从现识认为，Jekyll就是一个它为你提供网页前端等一系列框架操作，如果你不会操作的话，就这样。我现在只需要写博客即可。

### 安装

  	sudo apt install jekyll			//安装jekyll
  	
  	sudo apt install bundler		//安装bundler
  	
  	jekyll new my-blog				//新建jekyll文件夹
  	
	cd my-blog 						//进入文件夹
	
	bundle install
	
	bundle exec jekyll serve 		//编译并启动服务
	
	//打开浏览器 http://localhost:4000来检测是否启动成功

> 详细教程请移步http://jekyllcn.com/docs/installation/
### Ruby-Gems更换国内源
若是用的Ruby-Gems来安装jekyll，国内需要换源，否则会很慢，别问我为什么知道的...


 	1.查看现有源：gem sources -l
 	
	2.删除现有源：gem sources --remove https://rubygems.org/
	
	3.添加新源：gem sources -a http://gems.ruby-china.com/

## Git
Git是一种版本控制系统，作用呢，我打个比方🤪，就类似那些单机RPG游戏中存档功能，且每一次都会给你重新选个空白档存档，不会复制以前的存档，这样你就可以随时回到以前的一个状态。（单机游戏玩多了是这样的，哈哈哈...错乱ing）
>具体学习教程自己看书，这是电子书，冲！——>https://git-scm.com/book/zh/v2/

### 安装
	sudo apt-get install git 					//ubuntu安装git
	
	git config --global user.name "你的名字" 	//设置名字
	
	git config --global user.email "你的邮箱地址" //设置邮箱

## github
至于什么github的账号注册，仓库建立什么的，我这里就不说了，网上多的是，这里就讲述一下，在你安装jekyll之后，如何建立一个属于自己域名博客，而不是本地博客。（本地博客就是那个http://localhost:4000）

### 在自己有远程仓库的情况下
	cd myblog 						//进入自己创的文件夹
	
	git clone git@github.com:github.name/github.warehosename 				
	//克隆远程仓库，github.name为你注册github的账户名，github.warehosename为你创建的远程仓库名。
	
	jekyll new . --force			//把jekyll安装到当前目录 --force是在当前目录非空是使用。
	
	git add .						// 把当前目录下的所有文件都跟踪
		
	git commit -m "first commit" 	//设置一段提交的log信息
	
	git remote add origin git@github.com:github.name/github.warehosename 
									//增加一个远程服务器端
									
	git push -u origin main 		//推送至远程版本库


然后就可以进入到自己刚刚克隆的远程仓库了，进入settings，滑道网页底部。
这个沉浸在绿光的，冒着蓝色的域名，就是你的博客！
htpps://alte-yyk.github.io/ 这是我自己弄的博客，大家可以进去瞅瞅。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201207170424470.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQzNTEzNzc0,size_16,color_FFFFFF,t_70#pic_center)




