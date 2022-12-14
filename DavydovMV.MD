# Инструкция по работе с Git.![](LogoNew.jpeg)
https://github.com/KruglovDA/HW1108.git
## Установка Git
Чтобы установить Git можно воспользоваться данным [__сайтом__](https://git-scm.com/book/ru/v2/Введение-Установка-Git). В нем подробно расписанна установка на разные операционные системы.
___
## Основные команды для работы с Git
```
1. git init -  создание репозитория
    
    1.1 git init - создать новый проект в текущей директории.
    
    1.2 git init folder-name - создать новый проект в указанной директории
```
```
2. git add - индексация изменений

    2.1 git add - добавить в индекс все новые, изменённые, удалённые файлы из текущей директории и её поддиректорий
    
    2.2 git add text.txt -  добавить в индекс указанный файл (был изменён, был удалён или это новый файл)
    
    2.3 git add -i - запустить интерактивную оболочку для добавления в индекс только выбранных файлов
    
    2.4 git add -p - показать новые/изменённые файлы по очереди с указанием их изменений и вопросом об отслеживании/индексировании
```
```
3. git commit

    3.1git commit -m "Name of commit" - зафиксировать в коммите проиндексированные изменения (закоммитить), добавить сообщение
    
    3.2git commit -a -m "Name of commit" - проиндексировать отслеживаемые файлы (ТОЛЬКО отслеживаемые, но НЕ новые файлы) и закоммитить, добавить сообщение
```
```
4. git status - показать состояние репозитория (отслеживаемые, изменённые, новые файлы и пр.)
```
```
5. git log

    5.1 git log master - показать коммиты в указанной ветке

    5.2 git log -2 - показать последние 2 коммита в активной ветке

    5.3 git log -2 --stat - показать последние 2 коммита и статистику внесенных ими изменений
    5.4 git log -p -22 - показать последние 22 коммита и внесенную ими разницу на уровне строк

    5.5 git log --graph -10 - показать последние 10 коммитов с ASCII-представлением ветвления

    5.6 git log --since=2.weeks - показать коммиты за последние 2 недели

    5.7 git log --after '2018-06-30' - показать коммиты, сделанные после указанной даты

    5.8 git log index.html - показать историю изменений файла index.html (только коммиты)

    5.9 git log -5 index.html - показать историю изменений файла index.html, последние 5 коммитов (только коммиты)

    5.10 git log -p index.html - показать историю изменений файла index.html (коммиты и изменения)

    5.11 git log -G'myFunction' -p - показать все коммиты, в которых менялись строки с myFunction (в кавычках регулярное выражение)

    5.12 git log -L '/<head>/','/<\/head>/':index.html - показать изменения от указанного до указанного регулярных выражений в указанном файле

    5.13git log --grep fix - показать коммиты, в описании которых есть буквосочетание fix (регистрозависимо, только коммиты текущей ветки)

    5.14 git log --grep fix -i - показать коммиты, в описании которых есть буквосочетание fix (регистроНЕзависимо, только коммиты текущей ветки)

    5.15 git log --grep 'fix(ing|me)' -P - показать коммиты, в описании которых есть совпадения для регулярного выражения (только коммиты текущей ветки)

    5.16 git log --pretty=format:"%h - %an, %ar : %s" -4 - показать последние 4 коммита с форматированием выводимых данных

    5.17 git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short - мой формат вывода, висящий на алиасе оболочки

    5.18 git log master..branch_99 - показать коммиты из ветки branch_99, которые не влиты в master

    5.19 git log branch_99..master - показать коммиты из ветки master, которые не влиты в branch_99

    5.20 git log master...branch_99 --boundary -- graph - показать коммиты из указанных веток, начиная с их расхождения (коммит расхождения будет показан)
```
```
6. git diff

    6.1 git diff - сравнить рабочую директорию и индекс (неотслеживаемые файлы ИГНОРИРУЮТСЯ)
    
    6.2git diff --color-words - сравнить рабочую директорию и индекс, показать отличия в словах (неотслеживаемые файлы ИГНОРИРУЮТСЯ)

    6.3 git diff index.html - сравнить файл из рабочей директории и индекс

    6.4 git diff HEAD - сравнить рабочую директорию и коммит, на который указывает HEAD (неотслеживаемые файлы ИГНОРИРУЮТСЯ)

    6.5 git diff --staged - сравнить индекс и коммит с HEAD

    6.6 git diff master feature - посмотреть что сделано в ветке feature по сравнению с веткой master

    6.7 git diff --name-only master feature - посмотреть что сделано в ветке feature по сравнению с веткой master, показать только имена файлов

    6.8 git diff master...feature - посмотреть что сделано в ветке feature с момента (коммита) расхождения с master
```
```
7. git push

    7.1 git push origin :old_branch_name new_branch_name - применить переименование в удаленном репозитории

    7.2 git push origin master - отправить в удалённый репозиторий (с сокр. именем origin) данные своей ветки master
```
```
8. git branch — создание, перечисление и удаление веток
Работа с ветками — очень легкая процедура в git, все необходимые механизмы сконцентрированы в одной команде.

    8.1 git branch new-branch - создание новой ветки

    8.2 git branch -d new-branch - удаляет ветку, если та была залита (merged) с разрешением возможных конфликтов в текущую

    8.3 git branch -D new-branch - удаляет ветку в любом случае

    8.4 git branch -m new-name-branch - переименовывает ветку

    8.5 git branch --contains v1.2 - показывывает те ветки, среди предков которых есть определенный коммит

    8.6 git merge-base master new-name-branch - показывает коммит ответвления ветки new-name-branch от ветки master
```
## Пример начало работы. 
Создание нового репозитория, первый коммит, привязка удалённого репозитория с gthub.com, отправка изменений в удалённый репозиторий.
```
git init                      - создаём репозиторий в этой директории
touch readme.md               - создаем файл readme.md
git add readme.md             - добавляем файл в индекс
git commit -m "Initial commit"- создаем коммит
git remote add origin https://github.com:nicothin/test.git # добавляем предварительно созданный пустой удаленный репозиторий
git push -u origin master     - отправляем данные из локального репозитория в удаленный (в ветку master)
```
