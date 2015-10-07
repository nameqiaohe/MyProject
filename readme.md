# 练习使用GitHub
---------------------------
### 参考http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/0013743256916071d599b3aed534aaab22a0db6c4e07fd0000

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
		- 若当前命令行窗口没有关闭，则找到上一版本的版本号，输入前边几位即可，git会自动匹配，如：git reset 0269877
		- 若关闭了命令号窗口，则执行：git reflog，其中记录了每一次命令，也可以看到版本号
