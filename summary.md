## 一些git 日常使用功能汇总


- 创建git仓库：make emptydir; cd emptydir; git init 	#初始化git仓库

- git add file  										#将文件添加到仓库

- git commit -m "message" 								#提交文件到仓库

- git status 											#查看仓库状态

- git diff readme.md									#查看文件具体修改了什么内容

- git log 												#查看历史提交、修改内容

- git log --pretty=oneline								#查看一些简洁修改内容信息，包括commit id。用于回退历史版本。

- git reset --hard commit_id							#用于回退历史版本。

- git reset --hard HEAD^								#回退最近一次历史版本

- git reset --hard HEAD^^								#回退最近第二次历史版本

- git reset --hard HEAD~10								#回退第十次历史版本

- git reflog											#查看未来版本，回退之前版本

- git checkout -- file									#撤销工作区的修改



## 配置远程仓库连接

- ssh-keygen -t rsa -C "youemail@example.com" 			#获取ssh密钥

- 通过github.com 登录添加密钥到github ssh key中即可远程操作仓库


## 添加远程仓库

- 首先在github中 create  a new repo	创建新仓库

- git remote add origin git@github.com:name/repo.git	#将本地仓库与远程仓库关联

- origin 为git 默认远程仓库名字。

- git push -u origin master								#将本地内容推送到远程仓库上，master分支。

- git remote set-url origin git@github.com:newname/repo.gig　　#更改url地址

- git remote rename　　　　　　　#修改remote git仓库名字

- git remote --help　　　　　　　#查看帮助


## 克隆远程仓库

- git clone git@github.com:name/repo.git				#克隆远程仓库到本地


## 分支管理

- git checkout -b dev									#创建新分支dev，并切换到dev分支

- git branch dev										#创建新分支dev

- git checkout dev										#切换到分支dev

- git checkout --track origin/remotebranch              #切换远程分支并且复制到本地

- 上面 git branch dev;git checkout dev;等同于 git checkout -b dev

- git branch											# 查看当前的分支

- git merge dev											# 将dev分支成果合并到master分支

- git branch -d <name>									# 删除分支


## 分支冲突解决

#### 当不同用户提交分支不同内容时，出现冲突，需要进行合并。

- git log --graph --pretty=oneline --abbrev-commit      # 查看分支合并情况

- git branch -d dev　　　　　　　　　　　　　　　　　　# 将已合并的其他分支删除


