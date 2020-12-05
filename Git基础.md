#  Git 笔记

## Git的概念

Git是一种版本控制系统，所谓的版本控制系统便是记录各个版本，以便人们可以随时找回以前的原始数据，打个比方，类似与RPG游戏中的存档读档功能。（如果人生也可以存档读档就好了！）

## Git的特点

直接记录快照，而非差异比较。（意思是每个版本都信息都做成链接保存？）

近乎所有操作都是本地运行。（不受网络限制）

Git保证完整性。（哈希值）

Git一般只添加数据。（这样不会容易造成不可恢复操作）

## Git的三种状态

**已提交（committed）**、**已修改（modified）** 和 **已暂存（staged）**

- 已修改表示修改了文件，但还没保存到数据库中。
- 已暂存表示对一个已修改文件的当前版本做了标记，使之包含在下次提交的快照中。
- 已提交表示数据已经安全地保存在本地数据库中。

## Git的安装（ubuntu）（我用的ubuntu）

sudo apt install git-all（其他方法自己去找）

## 初次运行Git前的配置

git config --list --show-origin	//查看所有配置以及它所在文件

### 用户信息

git config --global user.name "yyk"

git config --global user.email "1812509145@qq.com"

### 检查配置信息

git config --list

### 获取帮助

git help <vebr>

git <vebr> --help

man git-<vebr>

## 取得项目的Git仓库

### 在工作目录中初始化新仓库

命令：git init

### 从现有仓库克隆

命令：git clone git://github.com/

## 记录每次更新到仓库

### 检查当前文件状态

命令：git status

### 跟踪新文件

命令：git add <filename> (跟踪后，该文件便是暂存文件了)

### 暂存已修改的文件



### 提交更新

命令：git commit



