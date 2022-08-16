# Инструкция по git

Для того, чтобы начать использовать git в Visual Studio Code требуется ввести в терминале команду 
* __git init__

Для начала пользования git`ом, необходимо инициализировать себя. Для этого требуется ввести две команды:
* __git config --global user.name "<ваше_имя>"__
* __git config --global user.email "<адрес_почты@mail.com>"__

Далее, чтобы git отслеживал файлы в папке требуется ввести команду 
* __git add <название файла>__

Если требуется указать комментарий по определенной версии файла, то в терминале вводим команду 
* __git commit -m "комментарий"__

Чтобы узнать статус нашего файла, то в терминале необходимо ввести команду 
* __git status__

Если мы хотим увидеть все коммиты, то в терминале вводим команду 
* __git log__ , чтобы выйти нажимаем __q__

Для того, чтобы перемещаться между коммитами в терминале вводим команду 
* __git checkout <первые 4 символа коммита, либо весь коммит>__

В случае, если мы хотим создать ветку, для чего-либо, то в терминале вводим команду 
* __git branch <название ветки>__

Для того, чтобы переключиться между ветками, в терминале вводим команду 
* __git checkout <Название ветки>__ 

Если мы хотим объединить наши ветки в одну, то сначала нам требуется перейти на главную ветку(master), а затем в терминале ввести команду 
* __git merge <Название ветки>__

Когда нам потребуется добавить картинку в файл, то мы можем сделать это через: 
* ![Текст, в случае если картинка не отобразится](Название картинки.формат)
Сама картинка должна находится в папке с файлом. 

Чтобы удалить ветку, то в терминале введем команду:
* __git branch -d <Название ветки>__ 