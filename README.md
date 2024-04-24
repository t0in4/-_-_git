# команды для создания локального репозитория git

**git init**        # инициализируем сам git

**git flow init**  # инициализируем git flow обеспечивающую определенную стратегию ведения контроля версий

                # в первой строчке пишем main, дальше все оставляем как есть.

**git branch**     # команда для создания новой ветки или проверки где я нахожусь


**git add -A**     # добавляем в git содержимого папки


**git checkout main** # переходим из develop в main, (или в master, если не меняли название первой папки)

**git merge develop** # соединяем содержимое (код) папки main и develop

**git add -A** 

**git commit -m "Наш код"** # добавляем запись о том, что сделали

**git log**        # смотрим журнал логов

# команды для пуша (отправки) локального репозитория в github

**git remote add origin https://github.com/*<имя аккаунта>*/*<название репозитория>*.git**    # добавляем в git имя репозитория и аккаунта github

**git push -u origin main** # добавляем в github файлы расположенные локально, по умолчанию название основной ветки master, мы поменяли на main когда  
                            # устанавливали git flow  
**чтобы запушить в репозиторий из командной строки  
в fine-grained token выбрать такие разрешения для репозитория

Contents         read and write  
 

# ошибки
## error: remote origin already exists.
**git remote rm origin** # удаляем удаленный репозиторий который мы неправильно инициализировали

##  ! [rejected]        main -> main (fetch first)
## error: failed to push some refs to 'https://github.com/../...git'
**git pull --rebase origin main** # обновили ссылки  

# обновить репозиторий после локальных изменений  
**git add .**  
**git commit -m "added stuff"**  
// if you create readme.md online  
// there will be an error ![rejected] master -> master (fetch first)  
// so, you have to git pull --rebase origin master  
**git pull**  
**git push origin master**  
