# Инструкция по работе с Git

![Git Logo here](https://upload.wikimedia.org/wikipedia/commons/e/e0/Git-logo.svg)

> I think that many others had been frustrated by all the same issues that made me hate SCM’s [Source Control Management systems], and while there have been many projects that tried to fix one or two small corner cases that drove people wild, there really hadn’t been anything like Git that really ended up taking on the big problems head on. Even when people don’t realize how important that “distributed” part was (and a lot of people were fighting it), once they figure out that it allows those easy and reliable backups, and allows people to make their own private test repositories without having to worry about the politics of having write access to some central repository, they’ll never go back.
***Linus Torvalds about Git***

##Общие сведения о системе управления версиями Git

**Git** (произносится «гит») — распределённая система управления версиями. Система спроектирована как набор программ, специально разработанных с учётом их использования в сценариях. Это позволяет удобно создавать специализированные системы контроля версий на базе **Git** или пользовательские интерфейсы. Например, Cogito является именно таким примером оболочки к репозиториям **Git**, а StGit использует **Git** для управления коллекцией исправлений (патчей).

**Git** поддерживает быстрое разделение и слияние версий, включает инструменты для визуализации и навигации по нелинейной истории разработки. Как и Darcs, BitKeeper, Mercurial, Bazaar и Monotone[en], **Git** предоставляет каждому разработчику локальную копию всей истории разработки, изменения копируются из одного репозитория в другой.

Удалённый доступ к репозиториям Git обеспечивается git-демоном, SSH- или HTTP-сервером. TCP-сервис git-daemon входит в дистрибутив Git и является наряду с SSH наиболее распространённым и надёжным методом доступа. Метод доступа по HTTP, несмотря на ряд ограничений, очень популярен в контролируемых сетях, потому что позволяет использовать существующие конфигурации сетевых фильтров. 

Более подробно см. на вики https://ru.wikipedia.org/wiki/Git


## Основные команды

*git init* - **инициализация репозитория**
*git status* - **вывод статуса репозитория на момент времени**
*git add* - **добавление файлу (файлам) версионности**
*git commit -m <message>* - **фиксация изменений**
*git log* - **вывод журнала изменений**                         
*git diff* - **вывод изменений по сравнению с предыдущим комитом**
*git checkout (hash number)* - **перемещение к определенному коммиту**
*git checkout master* - **перемещение к актуальному состоянию (последнему коммиту**

## Примеры выполения команд
`
    $ git status
    On branch master
    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
        modified:   instruction.md
    no changes added to commit (use "git add" and/or "git commit -a")
`


## Полезные ссылки по git

1. Общие сведения про git из вики https://ru.wikipedia.org/wiki/Git
2. [Учебник по Git на русском](http://git-scm.com/book/ru/v2)
3. [Официальный сайт Git](https://git-scm.com/)
4. [Еще немного про разницу Git и Github, централизованные и распределенные репозитории](https://tproger.ru/translations/difference-between-git-and-github/#part2)
5. [Список альтернатив вместо Git](http://lostapp.ru/soft/git)

## Команды по ветвлению

*git branch* - **команда для вывода списка веток**
*git branch <branch_name>* - **создание новой ветки**
*git checkout -b <branch_name>* - **создание новой ветки другим способом**
*git checkout <branch_name>* - **переключениена новую ветку**
*git merge <branch_name>* - **команда для слияния веток**
*git branch -d <branch_name>* - **команда для удаления ветки**

## Команды отмены

## Команды просмотра истории

## Команды тэгов

Тэги - это небольшие пометки важных изменений в истории проекта. Используются для удобства просмотра и поиска. 

*git tag* - **Просмотр имеющихся тэгов**

*git tag -l "string"* - **Поиск тэгов по строке-шаблону**. Например, поиск тэгов, относящихся к конкретной версии проекта.

*git tag -a <tag name> -m "commentary"* - **Создание аннотированного тэга**. -m и строка - это способ дать короткий комментарий к тэгу.

*git tag <tag_name>* - **Создание легковесного тэга**. Никаких комментариев и прочей информации.

*git show <tag_name>* - **Просмотр всей информации по тэгу**.

*git tag -d <tag_name>* - **Удаление тэга**.

