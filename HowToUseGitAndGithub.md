# Git和Github使用学习笔记
---
## Git安装

1. [官网下载](https://git-scm.com/downloads)安装包
2. 一路Next即可
3. 打开开始菜单，运行Git Bash即可(下文代码，全部在该窗口运行)


## Github第一面 ###

* sign in 建立账号+邮箱+登陆密码  
* sign up 登陆  

> 欢迎登陆全球最大同性社区  

> 看不懂英语？自己慢慢找翻译吧！！

## Git使用  

#### 初始设置
```
git config --global user.name "YourName"     
git config --global user.email "YourEmail@example.com"  
```
#### 设置SSH Key
```
ssh-keygen -t rsa -C "YourEmail@example.com"
```  
1. 再连着敲三个回车后会看到一个字符组成的图  
2. 找到下面目录：C:\Users\wwj\.ssh\  其中id_rsa是私有密钥,id_rsa.pub是公开密钥    
3. 打开公开密钥，复制  
4. 打开浏览器，登陆Github,进入个人设置页面，点击ssh，输入刚刚复制的内容  
5. 打开git bush，输入：
```
ssh -T git@github.com   
```

6. 出现“Hi YourName......” 则链接成功  

#### 建立本地仓库，并推送
```
git init  #初始化  
git status  #查看状态  
git add filename  #将文件修改内容加入到操作池  
git add .  #将所有文件修改记录都加入到strack操作池（这一行适用于大量文件修改时）   
git commit -m  "说明"   #这个说明会记录到github上
git remote add origin git@github.com:YourID/Re.git  #github用户名+新仓库名称   
git push -u origin master  #推送到远程仓库，master分支  
git log  #查看修改日志
```
#### 下载远程仓库

* 找到需要协作的仓库，fork到自己的远程仓库
* 打开仓库存放目录  
* 右键打开Git Bash  
```  
git init  #初始化  
git clone git@github.com:YourName/Re.git  #github用户名+新仓库名称  
```  
* 查看本地目录，若有clone仓库的同名文件夹，即下载成功
#### 修改远程仓库  
* 本地修改完文件后，对应文件打开Git Bash  
```
git status  #查看修改内容  
git add filename  #将修改记录添加到strack
git commit -m  "说明"#更新本地仓库，这个说明会记录到github上
git push  #将本地仓库修改推送到远程仓库
```
* 浏览器登录Github，找到fork的仓库，点击pull requests

> 12/20/2017 10:10:25 PM
