# git simple commands

## the first commit

- the 1 commit

- the second commit

- git --version
- git config --global user.email "xx@com"
- git config --global user.name "xx"
- git config --global --list

## create local git repository
- git -init
  
## make first commit

- press + for staging
- press the tick
- input commit message

## review the commit 

- git log //check
- check in the Timeline

## make second commit

- press + for staging
- press ... for commit all/amend

## github.com/

- create new repository
- git remote add origin https://... 
- git push -u origin main

## pull changes from github.com/

- edit on github readme.md and commit changes.
- click ... and select pull

## git clone

- open code without folder opened
- select clone repo or press F1 to input git:clone
- got to github and copy https url for the repo
- paste in the prompt, clone from url
- select a parent folder to local (github will create the repo folder inside the folder automatically) and click open

## git new branch

- click the left bottom label of main and get the dropdown menu for create a new branch.
- name the new branch name
- make commit
- click cloud icon to upload

## git remote

- git remote add origin https://sss.com/xxx.git
  // Adds a record to ./.git/config for remote named ＜name＞ at the repository url ＜url＞.
- git remote get-url origin
- git push <remote-name> <branch-name>
- git push origin
// Push the specified branch to , along with all of the necessary commits and internal objects. 
- git pull <remote>
- git pull --verbose

- git remote add origin https://... 
- git push -u origin main