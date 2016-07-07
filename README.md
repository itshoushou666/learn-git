# learn-git (git学习总结)

前提：
-公司仓库： git@github.com:gongsi/xxoo.git
-个人仓库： git@github.com:geren/xxoo.git

### Fork公司仓库，克隆个人仓库到本地，切换develop分支
###### (fork 开发仓库到个人仓库)
###### 克隆fork的个人仓库到本地
	- $git clone git@github.com:geren/xxoo.git
###### 添加开发仓库的源（使用git remote -v查看）
	- git remote add xxoo git@github.com:gongsi/xxoo.git
###### 获取远程开发仓库的分支和提交
	- git fetch xxoo
###### 拉取远程开发仓库源的develop分支
	- git checkout -b develop xxoo/develop
###### 推送到远程
	- git push -u origin develop 
### feature分支开发
###### 创建feature分支
	- git checkout -b some-feature develop
###### coding
	- git add .
	- git commit -m "xxxxxooooo"
###### 推送到远程
	- git push -u origin some-feature
### 合并远程开发仓库，及feature分支到本地develop,并推送到远程
###### 切回develop分支
	- git checkout develop
###### 将开发仓库develop分支合并到本地develop分支
	- git pull xxoo develop
###### 将本地feature分支合并到本地develop分支
	- git merge some-feature
###### 推送到远程
	- git push origin develop
###### 删除远程feature分支
	- git push origin --delete some-feature
###### 删除不存在对应远程分支的本地分支（删除本地feature分支）
	- git fetch -p
