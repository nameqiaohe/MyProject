# MyProject
我的项目，练习使用GitHub

- Step 1：注册GitHub
- Step 2：安装GitHub（Windows版）
      或者安装git（Linux）
- Step 3：创建项目（在网页上，右边）
-**      （1）项目名称：英文名 **
-**      （2）给项目添加一些描述 **
-**      （3）勾选 自动生成一个README.md文件 **
- Step 4：在项目主页的右边有一项：HTTPS clone URL，其下有一按钮，是用来复制项目地址，方便在Linux检出代码到本地。
- Step 5：进入Linux环境，创建一个目录，mkdir github，进入这个目录 cd github
- Step 6：git clone URL，URL就是刚才复制的地址
      将代码检出到本地
- Step 7：进入到项目目录，如MyProject，cd MyProject
        执行 git status，查看工作区/项目 的状态，若当前有修改，则会给出提示
:     比如：
        在当前目录下添加了一个文件test
        执行 git status，会提示说test未被跟踪
        将test添加为跟踪状态 git add test
        再次执行 git status，则提示说当前工作去是干净的
- Step 8：提交修改的代码，到本地：git commit
      弹出一个变更说明，需要添加一些修改信息，以便日后查看时，可以清楚的直到：谁在何时何地做了什么修改动作。
- Step 9：提交修改的代码，到github，即服务端：git push
      会提示输入 用户名、密码
