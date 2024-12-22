# git bush

在 Git Bash 中，默认支持以下键盘快捷键：

-   **粘贴**：`Shift + Insert`
-   **复制**：`Ctrl + Insert`

# git 使用

>   ~根目录下 touch .bashrc 添加以下两行代码，命令别称
>
>   alias git-log='git log --pretty=oneline --all --graph --abbrev-commit'
>
>   alias ll='ls -al'
>
>   解决中文乱码
>
>   1. gitbash执行：git config --global core.quotepath false
>   2. git安装目录/etc/bash.bashrc 文件最后加入下面两行代码
>   	- export LANG="zh_CN.UTF-8"
>   	- export LC_ALL="zh_CN.UTF-8"
>
>   配置ssh，添加id_rsa.pub到github,gitee,gitlab
>
>   ssh-keygen -t rsa 生成 RSA类型的密钥，cat 查看

`git init` 初始化本地仓库

 git config --global user.name "runoob"

git config --global user.email test@runoob.com

`git remote add origin ssh/http`

`ssh -T git@github.com` 测试远程仓库填的id_rsa.pub与本地id_rsa

`git pull ` 先pull一次，因为比如gitlab会自动添加个sb readme.md，github则不会

或者`git clone 远程仓库地址`

push之前检查远程仓库分支名与本地相同，否则会创建新的分支，使用`git branch -m 原分支 新分支`

`git push -u origin main:main` -u 等于`--set-upstream`

每次push之前一定要pull



`git add .` 添加所有有更改的文件到缓冲区

`git restore  目标文件` 暂存区 -> 覆盖 -> 工作区，目标文件（注意：完全确认覆盖时使用）

`git rm --cached 目标文件 ` 从暂存区移除文件，命令： 目标文件



`git commit -m "tips"`  提交到本地仓库

`git push` 然后提交到远程仓库



`git branch` 列出分支

`git branch 分支名` 创建一个新的分支

`git checkout -b 分支`  -b意味没有该分支就新建一个，有了就跳转

`git switch branch-name`：切换到指定分支

`git switch -c new-branch`：创建并切换到新分支

`git branch -d/D 分支` 删除分支(D:强制删除未合并的分支)

`git push origin --delete <branchname>` 删除远程分支



 `git merge branch-name`：将指定分支的更改合并到当前分支

eg: git merge origin/master 将远程master分支merge到当前分支上

对于出现的**conflict**(冲突)需要手动解决，然后再次提交



# Linux

一些常见的linux指令

`cd 路径` 进入指定路径的文件夹

`cd..` 返回上一目录

`vi` 使用vi编辑器编辑文件：

下是普通模式常用的几个命令：

-   **i** -- 切换到输入模式，在光标当前位置开始输入文本。
-   **x** -- 删除当前光标所在处的字符。
-   **:** -- 切换到底线命令模式，以在最底一行输入命令。
-   **a** -- 进入插入模式，在光标下一个位置开始输入文本。
-   **o**：在当前行的下方插入一个新行，并进入插入模式。
-   **O** -- 在当前行的上方插入一个新行，并进入插入模式。
-   **dd** -- 剪切当前行。
-   **yy** -- 复制当前行。
-   **p**（小写） -- 粘贴剪贴板内容到光标下方。
-   **P**（大写）-- 粘贴剪贴板内容到光标上方。
-   **u** -- 撤销上一次操作。
-   **Ctrl + r** -- 重做上一次撤销的操作。
-   **:w** -- 保存文件。
-   **:q** -- 退出 Vim 编辑器。
-   **:q!** -- 强制退出Vim 编辑器，不保存修改。
-   **G** 跳转到文档最后一行,**nG** 跳转到第n行,**gg** 跳转到文档第一行
