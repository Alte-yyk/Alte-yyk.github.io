# 通过SSH密钥对github仓库管理

## 一、远程仓库连接

git remote add origin git@github.com:username/repository.git	//username为github的用户名，repository为仓库名

git remote -v	//查看远程连接

## 二、设置密钥免密连接

ssh-keygen -t rsa -C "your.email.com"	//本地创建公私密钥对，your.email.com为你创建github账号时所用的邮箱号

ls ~/.ssh	//查看密钥

复制密钥到远程仓库 头像->setting->SSH and GPG keys->New SSH key

