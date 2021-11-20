# Git

## Initialization

`git init`

## Good commit

- atomic
- consistent
- commit early. commit often

**what(where):make**

what:
- feat
- test
- build
- refactor
- fix

refactor(element): ren ame parameter x

## Configuration

### General
#### Local config

    git config user.name "vasia"
    git config user.email vasia@ukr.net

    cat .git/config

#### Global config

    git config --global user.name "vasia"
    git config --global user.email vasia@ukr.net
    
    cat C:\Users\Sergey\.gitconfig

#### Show config

    git config --list
    git config --list —global

#### Delete config parameters

    git config --unset user.name
    git config --unset user.email

#### Delete user section

    git config --remove-section user

### Editor
   
    git config --global core.editor <PATH> + flags

### Aliases

    git config --global alias.c config

## Show git command's options:

    git config -h

## Show manual:

    git help config

## Listing command (LESS):

    find:   /
    find up:    n
    find down:  Shift + n
    exit:       q
 


## Arch

- Working directory
- Index
- Repository


## Often commands

    git status

### Add to Index

    git add script.js
    git add .
    git add -A

### Show details of commit

    git show l68124
    git show —pretty=fuller

## Multichange in file

    git add -p script.js

## commit without add: add+commit

    git commit -am 'message' // all changes for tracked

    git commit  -m 'message' .gitignore

## for untracked

    alias.commitall '!git add .; git commit'  // for folder
    alias.commitall '!git add -A; git commit'  // for project
    
## remove files

    git rm ...
    git rm -r ... // for folders
    git rm --cashed // delete from index only
    git rm -f // don't save change
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
 
    git checkout -b newbramchname // switch with no-commit changes
    git commit -am 'message'

    git branch -f master e543l
    
## ...

    git remote add upstream 


### List

Настройка локальной работы
Установка Git на локальный компьютер
    git clone
Информационные команды
    git status
    git diff


   список коммитов:
    git log 
    
   инфо про коммит
    git show
    git show n6323
    
   авторы файла
    git blame some.txt

   автор строки
    git blame some.txt | grep awesome

Работа с удаленной информацией
    есть ли измнения в удаленном репозитории:  
    git fetch  
    получить изменения из удаленного репозитория
    git pull

Работа с локальными изменениями
    git commit
    git push
    git merge
Буфер данных
    git stash
    git pop
Ветки
    git branch
    git branch delete
    git checkout
Работа с файлами
    git add
    git reset
    git reset --soft
    git reset --hard
    git reset HEAD
Конфигурация Git
    git alias
    user
    color
    .gitignore