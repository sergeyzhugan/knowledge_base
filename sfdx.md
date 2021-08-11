# SFDX

######

1. Create github repo
2. create sfdx project:

   sfdx force:project:create -n "MyProjectForGit"

3. create local git repo:
    
    git init

4. Add files:

   .vscode
   .forceignore
   .sfdx/
   .vscode/
   config/
   sfdx-project.json

   в .gitignore

5. Добавим удалённый репозиторий

   git remote add origin git@github.co/SFDX.git

6. Посмотрим добавлен ли репозиторий.

   git remote -v

7. Необходимо добавить папку force-app к отслеживаемым

   git add .

8. Создадим первый commit, который будет хранить структуру SF проекта.

   git commit -m "Init commit"

9. Отправим необходимую нам структуру на репозиторий:

   git push origin master

10. create scratch org

    sfdx force:org:create --definitionfile config/project-scratch-def.json --setalias dev --setdefaultusername

11. Check scrach org created:

    sfdx force:org:list

12. Add in .forceignore file:

    # Profiles
    **/profiles/**

13. open scratch org:

    sfdx force:org:open

14. Create objects and fields in scratch org
15. synchronize with project:

    sfdx force:source:pull

16. git add > commit > push
17. edit sfdx-prject.json: add namespace
18. create package:
 
    sfdx force:package:create --name "Formula One App" --description "Formula One App" --packagetype Managed --path force-app

19. To create the first release of your package, run the following command (all on one line):

    sfdx force:package:version:create --package "Formula One App" --definitionfile config/project-scratch-def.json --wait 10 --installationkeybypass

