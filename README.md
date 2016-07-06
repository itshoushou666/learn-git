# learn-git (git学习总结)

前提：
-公司仓库： git@github.com:gongsi/xxoo.git
-个人仓库： git@github.com:geren/xxoo.git

###Fork公司仓库，克隆个人仓库到本地，切换develop分支
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
