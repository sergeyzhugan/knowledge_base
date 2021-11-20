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

### General

    git config user.name "vasia"
    git config user.email vasia@ukr.net
    
    cat .git/config
    
    git config --global [user.name](http://user.name) "vasia"
    git config --global [user.email](http://user.name) "vasia@ukr.net"
    
    cat C:\Users\Sergey\.gitconfig

    git config --list
    git config --list —global
    
    git config --unset user.name // to delete user.name config parameter
    git config --unset user.email // to delete user.email config parameter
    
    git config --remove-section user // to delete user section

    git config --global core.editor <PATH> + flags

## Often commands

    git status
    git add script.js
    git add .
    git add -A
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