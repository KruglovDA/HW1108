#   Использование интеграции Git в  Visual Studio Code
## Введение ##    

Редактор **Visual Studio Code** (VS Code) стал одним из самых популярных для веб-разработки. Его популярность обусловлена множеством встроенных возможностей, в том числе интеграции с системой контроля исходного кода, а именно с Git. Использование возможностей Git из VS Code позволяет сделать рабочие процессы более эффективными и надежными.

## Предварительные требования ##

* **Git**, установленный на вашем компьютере.([Инструкция по установке](https://git-scm.com/book/ru/v2/%D0%92%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5-%D0%A3%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0-Git))
* **Visual Studio Code** последняя версия([Ссылка для скачивания](https://code.visualstudio.com/download)) , установленная на вашем компьютере. 

### Начало работы: ###

1) Прежде всего, чтобы воспользоваться преимуществами интеграции контроля исходного кода, следует инициализировать проект как репозиторий **Git**.
Откройте **Visual Studio Code** и запустите встроенный терминал. Вы можете открыть его, используя сочетание клавиш CTRL + ` ***Linux***, ***macOS*** или ***Windows***.
2) Используя терминал ((Ctrl+Shift+P)>Создать терминал)), создайте каталог для нового проекта и перейдите в этот каталог(команда -git test )
3) Создате репозиторий **Git** (Команда -git init),или вы можете сделать это в **Visual Studio Code** во вкладке Открыть папку.
4) Создайте файл (вкладка Создать файл). После этого на панели вы увидите, что рядом с именем вашего нового файла отображается буква **U**. Обозначение **U** означает, что файл не отслеживается, то есть, что это новый или измененный файл, который еще не был добавлен в репозиторий
5) Для того чтобы файл отслеживался,добавьте его в репозиторий или наберите в терминале команду git add .< file > ). После этого рядом с файлом появится буква **A**. **A** обозначает новый файл, который был добавлен в репозиторий.

    ![Удача не помешает,поэтому ](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR0ac4fOy6W6AFlaTAQXcSqn8yG2Sw52HpC6A&usqp=CAU)
