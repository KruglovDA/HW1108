# Конспект по контолю версий 
## Lesson 1
Install Git - https://git-scm.com/book/ru/v2/%D0%92%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5-%D0%A3%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0-Git

Install VSCode - https://code.visualstudio.com/ 

Starts VisualStudioCode

Open terminal: [ctrl]+[`]

Open the folder

Initialization git: *git init*

Create a new file

Add the file to the tracking: *git add "Conspect.docx"*

Edit the file

Save the file: [ctrl]+[s]

Create commit *git commit -a -m "Save commit"*

Show the diffeence *git diff*

Show the commit *gif log*

After applying this command you will be able the commit hash-sum and message

Show previous version *git checkout **the first four symbols of the hash-sum commit***

Show the current version *git checkout master*



q - выйти из многострочного просмотра

clear - очистить терминал

commits this is versions

Переименование файла расценивется как удаление старого файла и содзание нового

Консольная программа – это программа, управление в которой осуществляется без использования мыши...



## Practice 1

git config 

user.name=EVeklichHome

user.email=e.veklich@outlook.com

git status

git help

git status

**The first commit** git commit -m "Initial commit"

**Use the tab key**  git add .\02Notes.md

**Use the up and dybp keys**



***Внимание!***
При попытке выхода из многострочного просмотра нажатием клавиши "Й" ничего не выйдет - переключись на англ. раскладку


## Lesson 2

 Инструкция для работы с Markdown

### Выделение текста 

Курсив - обрамить текст (*) или (_). Например: *так*, _так_.

Полужирный - двойные (**) или (__). Например: **так**, __так__.

Адьтернативн способб выдел текста жрн или курсив нужны для совмещения: _текст м.б. курсиным и **полужирным**_

### Списки

Ненумерованный список - в начале текста ставь (*) или (+). Нпример:
* Эл-т 1
* Эл-т 2
* Эл-т 3
+ Эл-т 4

Нумерованный список - в начале ставь цифру. Например:
1. Первый
2. Второй

### Изображения

для вставки напиши: 
![текст если файла нет](name_file.jpg)
если файл изображения лежит в той же папке - укажи только имя файла, в противном случае, ?путь_целиком?

### Ссылки

### Таблицы

### Цитаты

### Команды в терминале

перенести потом сюда команды из терминала по лекции 2

## Practice 2

Внизу слева в строке состяния указано на какой ветке сейчас мы находимся

**git merge _name_branch_**

Use the command Merge in the branch you are going to merge into

Create and swich to a branch **git checkout -b _branch_new_** 

Конфликт возникает если в двух ветках внесены изменения ?в одну и ту же строку? 

Cancel the last merge **git merge --abort**

Если не работает отображение конфликтов при слиянии: File-->Preferences-->Settings; search: git merge; take off the first mark 

# Домашка 
## Тема 1
#### Задание 1
Сделать краткое руководство по git. В руководств описать использование изученных команд  и форматирование текста 

**Решение**

См. раздел "Конспект по контолю версий ", подразделы "Lesson 1" и "Practice 1". На описание форматирования текста сил не хватило:(

## Тема 2
### Exercise 1

Продолжить работу с файлом, начатую на Семинаре 1. Создать и слить как минимум 4 ветки. Обязательно создать конфликт и разрешить его. Архив с репозиторием и проделанной работой приложить к уроку.


# Dictionary

Branch - ветка

Merge - слияние

