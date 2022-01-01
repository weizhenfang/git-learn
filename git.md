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

## vs code

[video](https://www.bilibili.com/video/BV1dK411p7RF?from=search&seid=4112024852101568455)

提交：

1. 点击对号提交
2. 选择main

新建库：

1. 拉取推送
2. 同步
3. 新建库

推送：

1. github新建库
2. 点击省略号，选择推送
3. 选择库名
4. 选择main分支
5. 查看左下小云图标

创建新分支

1. 点击左下分支main
2. 创建新分支

创建 .gitignore

1. 添加文件
2. 选定本地main分支
3. 提交
4. 推送

拉取

1. 新建文件夹
2. vscode打开
3. 复制https地址
4. terminal中git clone 地址

登录

commit often, make it meaningful message!