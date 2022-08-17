![Git memes](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTkzW7A9hPQ47V7cHeFIofiGiR3onaYsh312OSjZTQ2zuvMpC1Je9gyXaO6PgXLgps5C5Q&usqp=CAU)

# Инструкция к работе с Git

## Настройка git

Необхлдимо задать имя и email
* ​`git config --­­global user.name "user.name"`
* `git config ­­global user.email "user.email"`

## Сводка основных команд Git

1. `git config` (Устанавливает элементы управления для локального сохранения проекта/файла)
2. `git init` (Инициализация/создание репозитория)
3. `git help` (Отображает всю необходимую информацию о командах git)
4. `git add` (Добавление новых файлов в репозиторий.)
5. `git status` (Показывает состояние репозитория (отслеживаемые, измененные, новые файлы и так далее))
6. `git log` (Перечисляет коммиты, сделанные в репозитории в обратном к хронологическому порядке)
7. `git commit` (Делает для проекта снимок текущего состояния изменений, добавленных в раздел проиндексированных файлов)
8. `git diff` (Вычисление разницы между любыми двумя Git деревьями)
9. `git clean` (Используется для удаления мусора из рабочего каталога)
10. `git checkout` (Позволяет исследовать ветки)
11. `git merge` (Включает изменения из названных коммитов в текущую ветку)
12. `git branch` (Команда для управления ветками в репозитории Git)

## Git log

После того, как вы создали несколько коммитов или же клонировали репозиторий с уже существующей историей коммитов. Одним из основных и наиболее мощных инструментов для этого является команда `git log`.

По умолчанию (без аргументов) `git log` перечисляет коммиты, сделанные в репозитории в обратном к хронологическому порядке — последние коммиты находятся вверху.

## Git Merge

**Синтаксис**

```bash
git merge [-n] [--stat] [--no-commit] [--squash] [--[no-]edit]
        [--no-verify] [-s <strategy>] [-X <strategy-option>] [-S[<keyid>]]
        [--[no-]allow-unrelated-histories]
        [--[no-]rerere-autoupdate] [-m <msg>] [-F <file>]
        [--into-name <branch>] [<commit>…​]
git merge (--continue | --abort | --quit)
```

**Описание**

Включает изменения из названных коммитов (с тех пор, как их история расходится с текущей веткой) в текущую ветку. Эта команда используется `git pull` для включения изменений из другого репозитория и может использоваться вручную для объединения изменений из одной ветки в другую.

Предположим, что существует следующая история и текущая ветвь является `master`:

```
          A---B---C topic
         /
    D---E---F---G master
```

Затем `git merge topic` воспроизведет изменения, внесенные в ветку `topic` так как она отклонилась от master (то есть `E` ) до текущей фиксации ( `C` ) поверх `master`, и запишет результат в новую фиксацию вместе с именами два родительских коммита и сообщение журнала от пользователя с описанием изменений.

```
          A---B---C topic
         /         \
    D---E---F---G---H master
```

Второй синтаксис (`git merge --abort`) может быть запущен только после того, как слияние привело к конфликтам. `git merge --abort` прервет процесс слияния и попытается восстановить состояние до слияния. Однако, если при запуске слияния были незафиксированные изменения (и особенно если эти изменения были дополнительно изменены после начала слияния), `git merge --abort` в некоторых случаях не сможет восстановить исходные (до слияния) изменения. Следовательно:

**Предупреждение** : запускать `git merge` с нетривиальными незафиксированными изменениями не рекомендуется: хотя это возможно, оно может оставить вас в состоянии, из которого трудно выйти в случае конфликта.

Третий синтаксис (`git merge --continue`) может быть запущен только после того, как слияние привело к конфликтам.

## Git branch

`git branch` – это команда для управления ветками в репозитории Git.

Ветка в Git'е — это просто «скользящий» указатель на один из коммитов. Когда вы создаёте новые коммиты, указатель ветки автоматически сдвигается вперёд, к вновь созданному коммиту.

Ветка, создаваемая первой в новом репозитории, по умолчанию называется `master`.

**Использование**

Чтобы создать новую ветку:

``` bash
git branch <branch-name>
```

Просмотреть список всех веток в текущем репозитории:

```bash
git branch
```

То же, включая удаленные (remote) ветки:

```bash
git branch --all
```

Переключиться на другую ветку:

```bash
git checkout <имя-ветки>
```

Создать новую ветку, указывающую на текущий HEAD:

```bash
git branch <имя-новой-ветки>
```

То же, плюс переключиться на нее одной командой:

```bash
git checkout -b <имя-новой-ветки>
```

Удалить ветку:

```bash
git branch -d <имя-ветки>
```

Взять текущие изменения (после последнего коммита) и создать из них новую ветку:

```bash
git stash
git stash branch <имя-ветки>
```

### Инструкция по работе с удаленным репозиторием
1. Переходим по ссылке (ссылка на репозиторий на GitHub)
2. Жмем на кнопку Fork (в списке наших репозиториев появился fork)
3. Клонируем к себе в папку
4. Открывает папку в VSC
5. выполняем git branch "название"
6. выполняем git checkout "назание"
7. Добавляем  файл 
8. Выполняем Коммит
9. выполняем git push (если git ругается, выполняем команду из подсказки)
10. на github выполняем pull request