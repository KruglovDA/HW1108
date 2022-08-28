# Введение в контроль версий. Git - быстрый обзор.
## **Git** - *это консольная утилита, для отслеживания и ведения истории изменения файлов, в вашем проекте*.

### __Основные понятия__:
    * Репозиторий -хранилище вашего кода и историю его изменений
    * Commit - точка сохранения вашего проекта
    * Hash - уникальный id комита

### __Основные команды__:
1. *git init* - инициализация/создание репозитория
2. *git add*, *git add --all* - добавляет все файлы проекта в будующий commit. 
Если хотим добавить конкретный файл то -
*git add <имя_файла>*
3. *git commit -m "<комментарий>"* - создает commit 
4. *git version* - выводит актуальную версию обновления git
5. *git status* - отображает состояние рабочего каталога и раздела проиндексированных файлов
6. *git log* -  перечисляет коммиты/ветки, сделанные в репозитории в обратном к хронологическому порядке
7. *git checkout <первые 4 символа hash/название папки>* - позволяет перемещаться между камитами/ветками.
8. *git checkout master - вернуться к актуальной версии
9. *git diff* - инициирует функцию сравнения источников данных Git — коммитов, веток, файлов и т. д
10. *git config --global user.name <...>*,*git config --global user.email <...>* - вводим наши данные в git
11. *git branch* - вывести на экран все ветки, и показать где находимся.
12. *git branch <название новой ветки>* - создать ветку
13. *git checkout -b   <название новой ветки>* - создать ветку и сразу на нее переключиться
14. *git merge <имя ветки для слияния с текущей> - объединяет ветки 
15. *git branch -d <название ветки на удаление> - удалить ветку
16. *git log --graph* - ключ -graf в связке с командой log позволяет отобразить коммиты в виде дерева

### __Полезное__:
 * Чтобы выйти из журнала в терминале воспользуйтесь кнопкой *Q*
 * Добавить/убрать маркировку статуса проекта в проводнике - заходим в настройки и ищем нужную функцию
 * Чтобы русифицировать VSC - скачиваем расширение *Russsian Language Pack*
 * Помним, что Git управляет сохраненными
файлами, а не теми, что в процессе
редактирования

### __Specific git-branch actions__:
-a, --all             list both remote-tracking and local branches
    -d, --delete          delete fully merged branch
    -D                    delete branch (even if not merged)
    -m, --move            move/rename a branch and its reflog
    -M                    move/rename a branch, even if target exists
    -c, --copy            copy a branch and its reflog
    -C                    copy a branch, even if target exists
    -l, --list            list branch names
    --show-current        show current branch name
    --create-reflog       create the branch's reflog
    --edit-description    edit the description for the branch
    -f, --force           force creation, move/rename, deletion
    --merged <commit>     print only branches that are merged
    --no-merged <commit>  print only branches that are not merged
    --column[=<style>]    list branches in columns
    --sort <key>          field name to sort on
    --points-at <object>  print only branches of the object
    -i, --ignore-case     sorting and filtering are case insensitive
    --recurse-submodules  recurse through submodules
    --format <format>     format to use for the output

### __Работа с изображениями__:
Чтобы добавить в проект изображение, необходимо пройти следующие шаги:
1. Добавляем новую ветку
2. В папку репозитория добвляем изображение
3. Командой git status проверяем статус проекта- теперь у нас появился еще однин файл. его мы игнорируем
4. чтобы полностью убрать надоедливые сообщени добавляем еще одни файл в проврднике, дать ему специальное название ".gitignore"
5. В этом файле указываем название док-та изображения
6. Сообщения больше не будут надоедать