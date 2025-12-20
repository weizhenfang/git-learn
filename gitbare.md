> git init --bare bare
> cd ../test
> git remote add bare ..\bare
> git push
> git push --set-upstream bare master
> git push

> git clone --bare test\.git test2
> git clone test2 test3
> git remote -v
    origin  D:/Projects/gitbare/test2 (fetch)
    origin  D:/Projects/gitbare/test2 (push)
> git status
> git pull

> git clone https://xxx felix_nonbare
> git branch
> git log
> ls -la

> git clone --bare https://.../felix felix_bare
> cd felix_bare
> ls -l
>
> git clone felix_bare felix
> git remote -v

> rm -rf felix_bare/
> mv felix/.git felix_bare
> ls -l
> rm -rf felix
> git config --bool core.bare true
> cd ..
> git clone felix_bare\ felix

> git config --bool core.bare

//natasha

> ssh natasha@ststor1
> sudo yum install git
> cd /opt
> ls -rtl /
> sudo git init --bare /opt/official.git
> cd /user/src/kodek/blog/
> git remote add dev_blog /opt/official.git/
> git config --global --add safe.directory /user/src/kodek/blog
> sudo git remote add ... 
> sudo cp /tmp/index.html .
> git add index.html
> git commit -m "xx"
> git push dev_blog master

> sudo mkdir -p /usr/src/kedeskrepos
> sudo git clone /opt/beta.git /usr/src/kedeskrepos
> cd /usr/src/kedeskrepos
> ls -a

> scp /tmp/index.html natasha@172.16.238.15:/tmp
> ssh natasha@172
> cd /tmp/
> ls -rlt
> sudo cp index.html usr/src/kodeskrepos/apps/
> cd usr/src/kodeskrepos/apps/
> ls
> git status
> git add .
> git commit -m ''
> sudo chmod 755 index.html
> sudo -i
> git push origin master

> git branch
> git checkout master
> git branch -d Xfusioncorp_apps
> git branch -D Xfusioncorp_apps


//

> sudo adduser git
> su git
> mkdir .ssh
> chmod 700 .ssh/
> touch .ssh/authorized_keys
> chmod 600 .ssh/authorized_leys
local > cat .ssh/id_ras.pub copy...
> vim .ssh/autorized_keys paste...
> ssh git@luke.xyz

> mkdir git
> chown git:git git/
> cd git
> ls -al
> mkkdir dotfiles
> mv dotfiles/dotfiles dotfiles.git
> cd dotfiles.git
> git init --bare

local> ra
> vim .git/config
> git push home master
> git log
> mkdir 

//
https://git-scm.com/book/en/v2/Git-on-the-Server-Getting-Git-on-a-Server

https://git-scm.com/book/zh/v2/%e6%9c%8d%e5%8a%a1%e5%99%a8%e4%b8%8a%e7%9a%84-Git-%e5%9c%a8%e6%9c%8d%e5%8a%a1%e5%99%a8%e4%b8%8a%e6%90%ad%e5%bb%ba-Git

$ git clone --bare my_project my_project.git
Cloning into bare repository 'my_project.git'...
done.

$ scp -r my_project.git user@git.example.com:/srv/git

$ git clone user@git.example.com:/srv/git/my_project.git




