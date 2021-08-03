# Git

## Initialization

`git init`

## Good commit name

**what(where):make**

what:
- feat
- test
- build
- refactor
- fix

refactor(element): rename parameter x

## Configuration

    git config [user.name](http://user.name) "vasia"
    git config [user.email](http://user.name) "vasia@ukr.net"
    
    cat .git/config
    
    git config --global [user.name](http://user.name) "vasia"
    git config --global [user.email](http://user.name) "vasia@ukr.net"
    
    git config --list
    git config --list —global
    
    git config --unset user.name
    git config --unset user.email
    
    git config --remove-section user

## Often commands

    git status
    git add script.js
    git add .
    git show l68124
    git show —pretty=fuller

## Multichange in file

    git add -p script.js

## commit without add

    git commit -am 'message'
    git commit  'message' .gitignore

## remove files

    git rm ...
    git rm -r ... // for folders
    git rm --cashed // only from index
    git rm -f // not save change
    git mv <old> <new> 

## branches

    git branch
    git branch -v
    git checkout newbranch
    git checkout -f branchname // chenges lose

    git checkout -f HEAD // delete changes

    git stash // save no-commit changes in stash befor checkout to another branch  
    git chechout another branchname
    git chechout mybranch
    git stash pop // return changes from stash after checkout from another branch