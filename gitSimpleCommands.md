
# Git

## 简单命令

> git init - 初始化仓库。
>
> git add . - 添加文件到暂存区。
>
> git commit -m '初始化项目版本' - 将暂存区内容添加到仓库中。
>
> git status

## 远程仓库push

让本地仓库与远程库相关联:

> git remote add [shortname] [url] 

    //添加一个新的远程仓库,指定一个简单的名字

> git remote add origin git@github.com:tianqixin/runoob-git-test.git

    说明：添加远程库，并命名为origin（git的默认叫法，可根据个人爱好修改），git@github.com/github的账号/github上远程库的名字.git

把本地版本库的内容推送到远程库上:

> git push -u origin master

    说明：实际上是把分支master推送到远程库origin，由于远程库是空的，我们第一次推送master分支时，加上了 -u 参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的的master分支关联起来，在以后的推送或者拉取时就可以简化命令。用git push origin master。

## git 配置

    $ git config --global user.name "Your Name"
    $ git config --global user.email "email@example.com"

显示当前的 git 配置信息：

>git config --list //显示当前的 git 配置信息：

编辑 git 配置文件:

> git config -e    # 针对当前仓库
> git config -e --global   # 针对系统上所有仓库

设置提交代码时的用户信息：

$ git config --global user.name "runoob"
$ git config --global user.email test@runoob.com

如果去掉 --global 参数只对当前仓库有效。

## git clone

>git clone [url] - 拷贝一个 Git 仓库到本地

> git clone https://github.com/tianqixin/runoob-git-test another-runoob-name

生成 SSH Key：
$ ssh-keygen -t rsa -C "youremail@example.com"

验证是否成功:

$ ssh -T git@github.com

    The authenticity of host 'github.com (52.74.223.119)' can't be established.
    RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
    Are you sure you want to continue connecting (yes/no/[fingerprint])? yes                   # 输入 yes
    Warning: Permanently added 'github.com,52.74.223.119' (RSA) to the list of known hosts.
    Hi tianqixin! You've successfully authenticated, but GitHub does not provide shell access. # 成功信息

$ git clone <版本库的网址> <本地目录名>

$ git clone https://github.com/jquery/jquery.git
或

$ git clone [user@]example.com:path/to/repo.git/

git clone支持多种协议，除了HTTP(s)以外，还支持SSH、Git、本地文件协议等

$ git clone http[s]://example.com/path/to/repo.git/

$ git clone ssh://example.com/path/to/repo.git/

$ git clone git://example.com/path/to/repo.git/

## git remote

> git remote //列出所有远程主机。

    origin

> git remote -v

    origin  git@github.com:jquery/jquery.git (fetch)
    origin  git@github.com:jquery/jquery.git (push)

> git remote show origin //查看该主机的详细信息

    remote origin
    Fetch URL: https://github.com/weizhenfang/markdown.git
    Push  URL: https://github.com/weizhenfang/markdown.git
    HEAD branch: main
    Remote branch:
        main tracked
    Local ref configured for 'git push':
        main pushes to main (local out of date)

命令用于远程主机的改名

> git remote rename <原主机名> <新主机名>

## git fetch

> git fetch <远程主机名> <分支名>

> git fetch origin master //取回origin主机的master分支。

$ git branch -r
origin/master

$ git branch -a
    * master
  remotes/origin/master

## git Pull
  
> git pull <远程主机名> <远程分支名>:<本地分支名>
>
> git pull origin next:master // 取回origin主机的next分支，与本地的master分支合并

## git push
将本地分支的更新，推送到远程主机

> git push <远程主机名> <本地分支名>:<远程分支名>

> git push origin master //将本地的master分支推送到origin主机的master分支

> git push -u origin main

# git Setup

[video](https://www.youtube.com/watch?v=8JJ101D3knE)

setup user
>git config --global user.name "w f"
>git config --global user.email e@f

setup editor
>git config --global core.editor "code --wait"

open code config
>git config --global -e

set CRLF for windows
>git config --global core.autocrlf true
>
>git config --help

[git config help](https://git-scm.com/docs/git-config)

[posh-git](https://github.com/dahlbyk/posh-git)

> git init
>
> git status
>
> git add .
>
> git add file1.txt
>
> git commit //Open editor
>
> git commit -m "Initial commit"
>
> echo world! >> file2.txt
>
> git commit -am "Add more mesage"
>
> rm file2.txt
>
> git status
>
> git ls-files
>
> git add file2.txt
>
> git ls-files
>
> git commit -m " remove unused code."
>
> git remove files.txt //remove fromm both working directory and the staging area.
>
> ls
>
> mv file1.txt file1.js
>
> git status
>
> git add .
>
> git status
>
> mkdir logs
>
> echo hello . logs/dev.log
>
> echo logs/ > .gitignore
>
> code .gitignore
>
> git add .gitignore
>
> git commit -m "add gitignore"
>
> git status
>
> git rm -h
>
> git ls-files
>
> git rm --cached -r logs/
>
> git ls-files
>
>git rm -r --cached .
>
>git add .
>
>git status -s
>
>git diff --staged
>
>git config --global diff.tool vscode
>
>git config --global difftool.vscode.cmd "code --wait --diff $LOCAL $REMOTE"
> git config --global -e
>
> git difftool --staged

### look history

> git log
>
> git log --oneline
>
>git show
>
> git show 6d6098e
>
> git show HEAD~1
>
>git show HEAD~1:logs/
>
> git show HEAD

### git objects

commits/Blobs(Files)/Trees(Direcgtory)/Tags

>git ls-tree HEAD~1
>
>git show 95d0

### restore file to previous version

> git restore filel.js
>
> git rm file1.js
>
>git status
>
>git commit -m "deleted file1.js"
>
> git log --oneline
>
> git restore -h
>
> git restore --source=HEAD~1 file1.js
>
>git status -s