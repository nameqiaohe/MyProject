# 练习使用GitHub
---------------------------
##### 参考http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/0013743256916071d599b3aed534aaab22a0db6c4e07fd0000

- Step 1：创建一个目录，mkdir protest
	- 进入这个目录，cd protest
- Step 2：将这个目录 变成 git可以管理的仓库：
	- git init
- Step 3：在当前目录下，创建一个文件readme.txt，在其中添加内容：
	- Git is a version control system.
	- Git is a free software. 
- Step 4：将readme.txt添加到仓库
	- （1）git add readme.txt
	- （2）git commit -m "wrote a readme file"
		- 注：-m 后输入的是 本次提交的说明，方便以后从 历史记录中查找改动记录。
- Step 5：git status 
	- 查看 工作区 的状态，比如：当前工作区有那些未被提交的改动文件
	- 若存在改动过的文件，可以通过 
		- git diff ---- 来查看具体做了哪些改动
	- 比较：
		- git status ----查看是否有 改动 未被提交
		- git diff ----查看具体的 改动信息

### 查看历史记录  
	git log
	或者 git log --pretty=oneline （一行显示）
- 记录中最近的一次提交 在最上边
- log中那一长串 数字+字母，是commit id（版本号）

### 回退 git reset
	git reset --hard HEAD
- 回到上一版本
	- 比如：从版本1 一直修改到 版本3，此时，想回到版本2，执行：git reset --hard HEAD
	- 若又想从 版本2 回到 版本3：
		- 若当前命令行窗口没有关闭，则找到上一版本的版本号，输入前边几位即可，git会自动匹配，如：git reset --hard 0269877
		- 若关闭了命令号窗口，则执行：git reflog，其中记录了每一次命令，也可以看到版本号

### github上创建远程仓库
- Step 1：登录GitHub，右上角点击Create a new repo...
- Step 2：输入仓库名（给仓库起一个名字），其他默认，然后点击Create repository
    - 这就在GitHub上创建了一个仓库
    - 接下GitHub会有一些提示信息，如下
### 
    …or create a new repository on the command line

        echo # protest >> README.md
        git init
        git add README.md
        git commit -m "first commit"
        git remote add origin https://github.com/nameqiaohe/protest.git
        git push -u origin master

    …or push an existing repository from the command line

        git remote add origin https://github.com/nameqiaohe/protest.git
        git push -u origin master

    …or import code from another repository

        You can initialize this repository with code from a Subversion, Mercurial, or TFS project.

- Step 3：接下来将本地仓库提交到GitHub上，在本地仓库目录下执行 

    （1）git remote add origin https://github.com/nameqiaohe/protest.git
添加后，远程库的名字就是origin，这是Git默认的叫法，也可以改成别的，但是origin这个名字一看就知道是远程库。
接下来，就可以把本地库的所有内容推送到远程库上：
    （2）git push -u origin master
把本地库的内容推送到远程，用git push命令，实际上是把当前分支master推送到远程。
由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。
推送成功后，可以立刻在GitHub页面中看到远程库的内容已经和本地一模一样。
