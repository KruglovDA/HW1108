
## **Краткое руководство по работе с Git**

### **Консольные команды Git:**
+ git log — позволяет вызывать список действий и сохранений.
  + git log --graph — позволяет отобразить коммиты в виде дерева.
+ git init — позволяет создать репозиторий в папке на локальной машине.
+ git add — позволяет отслеживать добавленные файлы,
+ git commit -m <комментарий> — добавляет комментарий к коммиту.
    + git commit -a -m <комментарий> добавляет новый коммит и комментарий к нему
+ git diff — показывает разницу между версиями,
+ git chechout —  позволяет переключиться между разными ветками.
+ git status - Позволяет  проверить индексацию изменений и увидеть файлы, которые не отслеживаются.
+ git branch - Позволяет знать ветку на которой мы находимся. 
  + git branch <название новой ветки> - Позволяет создать новую ветку.
  + git branch -m <old_branch_name> <new_branch_name> позволяет изменить название ветки
+ git merge <имя ветки> - позволяет провести слияние слияние указанной ветки с текущей 
  + git merge –abort - Позволяет отменить слияние, которое вы только что выполнили.
+ git ignore - позвоялет исключить лишние файлы из загрузки в Git
+ git reset - отменяет изменения, перенося ссылку на ветку назад, на более старый коммит.
+ git revert - в отличие от git reset подходит для работы с удаленными ветками.

### **Работа с удаленным репозиторием**
#### *Консольные команды*
+ git pull - позволяет скачать всё из текущего удаленного репозитория. Автоматически делает merge с текущей версией!
+ git clone - позволяет склонировать внешний репозиторий в локальный.
+ git push - позволяет отправить свою версию репозитория на удаленный репозиторий
#### *Pull request*
1. Делаем fork интересующего репозитория
2. Делаем git clone для появления локальной версии
3. Создаем ветку в которой будем проводить изменения
4. Проводим изменения
5. Отправляем свою версию на **свой аккаунт** в gitHub
6. На странице своей копии репозитория на GitHub, выбираем ветвь feature и жмем кнопку Pull Request.
7. Далее попадем на предпросмотровую страницу, на которой можно ввести название и описание изменений. 


### **Для начала работы с Git**
[X] Сделать папку репозиторием через команду **git init**

[X] Создаить файл и сохранить его

[X] Добавить файл через git add [имя]

[X] Делаем первый коммит "Initial commit"

[X] Проверяем что всё прошло успешно через git log

#### *Инструкция сделана на основе:*
[Конспект лекции №1 "Знакомство с контролем версий"](https://gbcdn.mrgcdn.ru/uploads/asset/3937510/attachment/187904bc7fa424abc113f5dda8b497ff.pdf)  
[Конспект лекции №2 "Установка и настройка системы контроля версий"](https://gbcdn.mrgcdn.ru/uploads/asset/3937511/attachment/83b2469d100de1c91ac3549b06705e87.pdf)  
[Конспект лекции №3 "Углубляемся в контроль версий"](https://gbcdn.mrgcdn.ru/uploads/asset/3937512/attachment/44012210dadb0a26c2d39b87e80b9db0.pdf)  