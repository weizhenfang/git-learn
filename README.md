# git Setup

setup user
>git config --global user.name "w f"
>git config --global user.email e@f

setup editor
>git config --global core.editor "code --wait"

open code config
>git config --global -e

set CRLF for windows
>git config --global core.autocrlf true

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
> git ls-files
> git add file2.txt
> git ls-files
> git commit -m " remove unused code."
> git remove files.txt //remove fromm both working directory and the staging area.
> ls
> mv file1.txt file1.js
> git status
> git add .
> git status


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

> git rm --cached -r logs/
> git ls-files

commit often, make it meaningful message