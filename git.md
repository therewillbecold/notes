# Git

git是一个版本管理工具

官方文档 [https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)

## 安装

windows下安装cmder时, 会同时安装好git-for-windows

mac下安装

- CLI: command line interface 命令行接口
- GUI: graphical user interface 图形化接口(图形化界面)

让git status显示中文文件名
执行下面这个命令
git config --global core.quotepath false

## 基础命令

查看当前仓库的状态
git status

把一个路径或者文件添加到暂存区
git add <path>

如 git add .  可以把当前的文件夹内的改变添加到暂存区

把改动提交到本地仓库
git commit -am <message>

把本地仓库的commit历史提交到远程仓库
git push origin master

### 分支操作

建立一个新的分支
git branch -b <分支名>
如: git branch -b liaoliao

切换到一个已经存在的分支
git checkout liaoliao

列出当前所有的分支
git branch -l

列出所有分支, 包括远程仓库的分支
git branch -la

### 远程仓库

给当前的本地仓库添加一个远程仓库

 git remote add github-liaoliao git@github.com:therewillbecold/whatever.git

列出远程仓库
~]$ git remote -v
输出:
> github-liaoliao git@github.com:therewillbecold/whatever.git (fetch)
github-liaoliao git@github.com:therewillbecold/whatever.git (push)
origin  git@github.com:therewillbecold/notes.git (fetch)
origin  git@github.com:therewillbecold/notes.git (push)

推送到远程仓库
git push origin master

