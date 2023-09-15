![Logo](лого.jpeg)
# Работа с Git
## 1. Проверка наличия установленного Git
В терминале  выполнить команду `Git --version`. Если Git установлен, появится сообщение с информацией о версии программы, иначе будет сообщение об ошибке.
## 2. Установка Git
Загружаем последнюю версию Git с [сайта](www).Устанавливаем с настройками по умолчанию.
## 3. Настройка Git
При первом использовании Git необходимо представиться. Для этого нужно ввести в терминале 2 команды:
``Bash
git config --global user.name "Ваше имя английскими буквами"
git config --global user.email ваша почта
``
## 4. Инициализация репозитория 
В терминале выполнить команду `Git init`. Данная команда создаст скрытую папку в выбранном репозитории и начнет отслеживать изменения в находящихся в выбранной папке файлов.
## 5. Запись изменений в репозиторий
###### Для просмотра статуса изменяемого файла исмользуется команта `Git status`;
###### Для подготовки произведенных изменений к записи версии используется команта `Git add "Имя подготавливаемого файла с расширением`. Также с помощью данной команды можно подготовить к записи все файлф в папке, для этого необходимо после команды поставить *, вместо имени файла, вот так `Gid add *`;
###### Для создания коммита используется команда `Git commit - m "комментарий"`
###### Для того, что бы увидеть разницу между текущим файлом и закоммиченным используется команда `Git diff`
## 6. История просмотра коммитов
В терминале выполни команду `Git log`. Данная команда выведет на экран истории всех коммитов с их хеш-кодами.
## 7. Перемещение между сохранениями
###### Для перемещения используется команда `Git checkout "хеш-код"`, Хеш-код каждого изменеия можно увидеть при выполнении команды `Git log`.
###### Для возврата к актуальному состоянию используется команда `Git checkout master`, либо `Git switch -`.
## 8. Игнорирование файлов
Для пого, чтобы исключить из отслеживания в репозитории определенные папки или файлы необходимо создать там файл `.gitignore` и записать в него их названия или шаблоны, соответствующие таким файлам или папкам.
## 9. Создание веток в Git
По умолчанию имя основной ветки в Git - `master`
Создать ветку можно командой:
``
git branch <имя новой ветки>
``
Для просмотра списока веток воспользоваться командой `Git branch`.
Так же можно создать ветку и сразу переключится на неё, для этого используется комбинированная  команда `Git checkout -b <Имя новой ветки>`, либо командой `Git switch -c <Имя новой ветки>`
Для переключения между ветками используется команда `Git switch <Имя ветки на которую хотим перейти>`
## 10. Слияние веток и разрешение конфликтов
Для слияния выбранной ветки с текущей нужно выполнить команду:
``
Git merge <Имя выбранной ветки>
``
Если была изменена одна и та же часть часть файла в обеих ветках, то может возникнуть конфликт, который потребует участия пользователя.
В случае конфликта интерфейс Visual Studio Code предлогает различные способы разрешения. 
## 11. Удаление веток
Удаление ветки возможно только из другой, Сиситема выдаст ошибку при попытке удаления текущей ветки. Само удаление ветки осуществляется командой `Git branch -d <Имя удаляемой ветки>`. 
При попытке удалить неслитую ветку, система укажет на это и предложит для начала слить данную ветку, Если же в слияние данной ветки нет необходимости, то можно принудительно её удалить командой `Git branch -D <Имя удаляемой ветки>`.