# **git常用命令**

### 常用命令

​	git clone  +url(下载地址)	

#### 	本地库初始化	

​		git init    初始化本地仓库

#### 	设置签名

​		git config user.name  aaa    创建项目级别用户

​		git config user.email  aaa@163.com  创建项目级别邮箱

​		git config --gloub user.name     创建全局用户

​		git config --gloub user.email   创建全局邮箱

### 基本操作

#### 	查看状态

​		git status  查看工作区,暂存区状态

#### 	添加

​		git add [file name] 将工作区的"新建/修改" 添加到暂存区

#### 	提交

​		git commit -m "message" [file name] 将暂存区的内容提交到本地库

#### 	查看历史记录

​		git log 查看历史记录  空格向下翻页,b向上翻页 , q 退出

​		git log --pretty =oneling  在一行显示历史信息

​		git log --oneling  在一行显示历史信息  (部分)

​		git reflog   显示当前的head 位置

#### 	前进后退

​		git reset --hard [局部索引值]      改变当前版本

​		git reset  --hard HEAD ^   一个^表示后退一步,n个表示后退n步

​		git reset --hard HEAD ~n    表示后退n步

#### 	reset 命令的三个参数

​		-- soft  仅仅在本地移动HEAD指针

​		--mixed  在本地移动HEAD指针 ,重置暂存区

​		--hard 在本地移动HEAD指针,重置暂存区和工作区

#### 	比较文件差异

​		git diff [文件名]  将工作区中的文件和暂存区的文件进行比较

​		git diff [本地库中历史版本 ]" "[ 文件名] 将工作区的文件和本地历史记录比较

### 分支管理

#### 	分支操作

​		git branch [分支名称]               创建分支

​		git barnch -v                         查看分支

​		git checkout [分支名称]            切换分支

#### 	合并分支

​		git checkout [被合并的分支名称]   

​		git merge  [有新内容的分支名称] 

#### 	冲突的解决

​		 第一步： 编辑文件， 删除特殊符号
​		 第二步： 把文件修改到满意的程度， 保存退出
​		 第三步： git add [文件名]
​		 第四步： git commit -m "日志信息"
​		 注意： 此时 commit 一定不能带具体文件名

### 连接远程库

#### 	创建远程库的别名

​		git remote -v 查看当前所有远程地址别名
​		git remote add  [别名]" "[远程地址]    创建别名

#### 	推送

​		git push [别名]' '[分支名]   推送到远程库

#### 	克隆

​		git clone [远程地址]  克隆到本地

#### 	拉取

​		pull=fetch+merge
​		 git fetch [远程库地址别名]' '[远程分支名]
​		 git merge [远程库地址别名/远程分支名]
​		 git pull [远程库地址别名]' '[远程分支名]



​	



