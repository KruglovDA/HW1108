Файл от Добычиной Вероники Юрьевны
# Instructions for working with Git.

*Git - это система контроля версий, она дает возможность контролировать версии проекта, **ХРАНИТЬ** различные версии и **ПЕРЕМЕЩАТЬСЯ** между ними.*
## Начало работы с Git

1. Для использования контроля версий необходимо установить и настроить Visual Studio Code и Git.
2. Для того, чтобы отслеживать изменения, все файлы необходимо где-то хранить, для этого создаем новую папку, называем ее как угодно.
Из папки нужно будет сделать репозиторий.
3. Запускаем Visual Studio Code. Чтобы Visual Studio Code мог взаимодействовать с папкой ее нужно открыть:
Файл-открыть папку.
4. Чтобы Git начал контролировать все, что происходит в этой папке и начал сохранять версии, необходимо дать ему такую команду, для этого нужно открыть терминал для ввода команд. Терминал-Создать терминал.
5. Перед тем как дать команду сохранять версии, нужно проверить, что Git настроен:
в терминал вводим команду git --version, если Git установлен и настроен правильно, то на экране увидим текущую версию программы.
6. Далее вводим, команду с помощью которой Git начнет отслеживать все, что происходит в этой папке, создаст репозиторий: git init.
7. С помощью команды git status, можно узнать все, что происходит в папке.
8. Чтобы начать сохранять, нужно создать новый файл в нашей папке: ПКМ - создать файл. Добавляем название файла и начинаем в нем работать.
9. После того как сделали изменения в файле, его нужно сохранить: Ctrl+S, далее проверить статус, уже знакомой командой git status.
Чтобы вызвать ту команду, которую писали необязательно писать ее заново, можно нажать "стрелка" на клавиатуре,
откроются те команды, которые писали ранее и можно между ними переключаться.
10. Что бы Git начал отслеживать файлы, которые появились, нужно использовать команду: git add и указать тот файл, который, необходимо добавить.
С помощью клавиши Tab, можно переключаться между названиями файлов и папок, которые находятся в репозитории и найти название файла.
11. Еще раз проверить статус, чтобы узнать, что поменялось: git status. Теперь Git начал отслеживать наши файлы.
12. Можно сохранить те изменения, которые совершили до этого с помощью команды git commit -m "пишем комментарий к этому сохранению".
Первый комментарий обычно пишут Initial commit (первое сохранение).
Чтобы выполнить commit без команды add: git commit -a -m"".
13. Далее по кругу, добавляем еще изменений, сохраняем изменения в файле Ctrl+S, добавляем файл и сохраняем git add + git commit.
14. Когда есть несколько сохранений, можно переходить от одной версии файла к другой.
Сначала нужно узнать, какие версии существуют командой git log (журнал изменений).
15. С помощью команды git checkout + первые 4 символа нужного сохранения, можно перекидываться между разными версиями.
16. Для того, чтобы дальше работать над файлом, необходимо вернуться в актуальное состояние, с помощью команды git checkout master.

## Ветки в git и их использование:
1. Команда git branch выводит на экран список имеющихся веток. По звёздочке видно, в какой ветке находимся.
2. Чтобы поработать над блоком в отдельной ветке, необходимо её создать, с помощью команды git branch, но помимо этой команды необходимо указать имя
новой ветки. Например, git branch branches_git.
3. Команда git checkout branches_git позволит перейти на вновь созданную ветку.
4. После редактирования новой ветки, нужно сохранить изменения Ctrl+S и сделать команду git commit -a -m "коментарий" Например, (добавили инструкцию в ветку branches_git).
5. Когда закончим редактировать новый блок, можно будет залить его на основную ветку master.
Перед этим проверим наше расположение, git branch.
Взглянем на текущий статус, git status, убедимся, что всё сохранено.
- Перейдем на основную ветку, с помощью команды , git checkout с указанием название ветки, в которую необходимо переместиться. git checkout master.
- Находясь на основной ветке master, сольем ветки с помощью команды git merge
и укажем ветку, которую необходимо добавить. Например, git merge branches_git.
6. Ветка branches_git больше не нужна, можно её удалить. Для этого используется команда git branch -d branches_git. Где параметр d сокращение от deleted (с англ. удалить), а branches_git имя удаляемой ветки.
### Объединение ветвей с разной информацией, работа с конфликтами: 
1. Когда один и тот же текст в разных ветках написан по-разному, при их соединении возникнет конфликт.
Например, когда из ветки master что-нибудь написано в ветке branches_git и сделан здесь коммит внутри master, git commit -a -m "текст комментария".
2. Чтобы соединить векти, находясь на ветке master, с помощью команды git merge branches_git зальем изменения из ветки branches_git.
Изменения пройдут, но с конфликтом. 
У Visual Studio Code есть возможность принять текущую версию, которая пришла с другой ветки (Current Change) или оставить и сравнить оба варианта.
Далее команда git commit -a -m "слили изменения с учётом конфликтов из ветки branches_git"
Проверить status и log.


## Список команд Git:

* git config - задать или изменить имя пользователя и адрес электронной почты;

* git --version - увидеть текущую версию Git;

* git status - показывает текущее состояние Git, есть ли изменения, которые нужно закоммитить сохранить;


* git init — создать репозиторий в папке, в которой Git начнет отслеживать изменения;

* git add название файла. расширение — отслеживать добавленные файлы;

* git commit -m "" - сохранить с комментарием;

* git commit -a -m "текст комментария" —  команда add  соединена с командой commit, отследит добавленные файлы и сохранит текущее состояние;

* git diff — показать разницу между версиями;

* git chechout имя ветки на которую хотим переключиться (первые 4 символа из сохранения) — переключиться между разными версиями;

* git checkout master - переключиться на коммит в котором работаем;

* git branch - вывести список веток в репозитории;

* git branch имя новой ветки - создать новую ветку;

* git branch имя ветки - удалить ветку;

* git log — вызывать список действий и сохранений, отображает список последних коммитов в порядке выполнения, с конца в начало;

* git log --stat --graph - история в виде дерева;

* git log --graph - отображает граф с ветвлениями и историей слияний;

* git log -p - выводит то же, что и git log, но еще и с изменениями в файлах, т.е расширенный вывод истории;

* git log --oneline - выводит каждый коммит в одну строку;

* git merge - используется для слияния одной или нескольких веток в текущую.


## Инструкция по работе с изображениями:

● Чтобы вставить изображение в текст, достаточно написать следующее:
! []()

В квадратных скобках мы укажем текст, который будет выводиться, если изображение не загрузится. А в круглых скобках имя файла, из которого необходимо изображение достать. Например, ![Привет, это Феник](Fenik.jpg)


## Инструкция для работы с Markdown:

● Чтобы выделить текст курсивом, необходимо обрамить его звёздочками (*).

Например, *вот так* .

● Чтобы выделить текст полужирным, необходимо его обрамить двойными звёздочками
(**).

Например, **вот так**.

● Чтобы добавить ненумерованные списки, необходимо пункты выделить звёздочкой
(*).

Например, вот так:
* Элемент 1
* Элемент 2
* Элемент 3

● Чтобы добавить нумерованные списки, необходимо пункты просто пронумеровать.

Например, вот так:
1. Первый пункт
2. Второй пункт

● Чтобы выделить текст курсивом, необходимо обрамить его звёздочками (*) или знаком
нижнего подчёркивания (_).

Например, *вот так* или _вот так_.

● Чтобы выделить текст полужирным, необходимо его обрамить двойными звёздочками
(**) или двойным нижним подчёркиванием (__).

Например, **вот так** или __вот так__.

● Альтернативные способы выделение текста жирным или курсивом, нужны для того,
чтобы мы могли совмещать оба этих способа.

Например, _текст может быть выделен
курсивом и при этом быть **полужирным**._
