# help-repository

Записываю сюда основные команды, моменты по созданию репозиториев и варианты маркдауна, которые обязательно мне пригодятся

Для Git-bash

!Стоит помнить, что при помощи стрелок можно передвигаться между последними командами.

1)pwd - показывает текущее местоположение в файлах

2)cd - меняет местоположение. Пишется - cd имя-папки. При пробелах в названии используются "". Можно использовать tab для автозаполнения, вроде написать firs от названия first-project, и гит дозаполнит сам.

3)ls - выводит содержимое директории. При добавлении -a выводит скрытые файлы.

4)touch - создаёт файл. Желательно писать расширение также.

5)mkdir - создаёт директорию

6)cp - копирует файл. cp что_копируем куда_копируем

7)mv - двигает файл. Синтаксис как у предыдущего cp

8)cat - читает файл. Пишется вместе с называнием

9)rm - удалить файл перманентно. rmdir удаляет пустую директорию, но с -r удаляет директорию с содержимым.

10)git status - выводит состояние репозитория

11)git log даёт список истории коммитов

---

Для Github - памятка по созданию репозитория и связыванию его с локальным

1)Настроить через git-bash хаб при помощи 2 команд: $ git config --global user.name "ваше имя или ник латиницей" |, потом| $ git config --global user.email ваша электронная почта

2)Создать SSH-ключ. Для этого:

2.1)включить гит-баш. В домашней папке написать $ ls -la .ssh/  | если вывод пустой, всё в порядке. В ином случае ключи создавались, их надо удалить если генерировали не вы.

2.2)сгенерировать ключи при помощи одной из 2 комманд: $ ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub" |или| $ ssh-keygen -t rsa -b 4096 -C "электронная почта, к которой привязан ваш аккаунт на GitHub" | можно поставить пароль после этого.

2.3) После выполнения ssh-keygen в директории ~/.ssh есть два файла — id_ed25519 и id_ed25519.pub (или id_rsa и id_rsa.pub — в зависимости от того, какой алгоритм вы использовали). Скопируйте содержимое файла с публичным ключом в буфер обмена. После пишем команду $ pbcopy < ~/.ssh/id_rsa.pub |для ed25519 надо написать:|  $ pbcopy < ~/.ssh/id_ed25519.pub

2.4)в гитхабе создать через настройки профиля новый SSH-ключ. В поле key надо вставить значение ключа из прошлого пункта.

2.5)в гит-баше ввести $ ssh -T git@github.com

3)создать репозиторий на ПК, в баше перейдя в нужную папку в которой мы его создадим и напечатав команду git init

4)связать удалёенный репозиторий и локальный, написав git remote add origin git@github.com:%ИМЯ_АККАУНТА_ГИТХАБА%/first-project.git |После этого стоит убедится, что всё удалось:| git remote -v

4)переместить в репозиторий файлы и при помощи git add заставить гит понимать что они к нему относятся. При помощи флага --all добавить можно все файлы

5)сделать коммит при помощи git commit. При добавлении -m можно в "" написать комментарии, что очень рекомендуется

6)загрузить изменения на удалённый репозиторий с помощью команды в баше git push -u origin main |если это не работает, менять main на master. Когда сработало, повторять когда угодно.

---

Памятка маркдауна, клонирования репозиториев и форкинга:

1)решетки от 1 до 6 создают заголовки от большего к меньшему

2)можно добавить черту при помощи 3 последовательных минусов

3)два пробела для разрыва строки

4)два раза enter для нового параграфа (это сложно забыть)

5)текст заключается в зведочки для курсива

6)для полужирного шрифта ставятся двойные звездочки

7)для зачеркивания ставят двоные волнистые линии ~

8)для нумерованного списка ставят в начало строк цифры с точками

9)ненумерованный создаётся звёздочкой с пробелом в начале строк

10)для ссылки текст который должен её содержать заключается в круглые скобки, а адрес ссылки в круглые. Между скобками нет пробела. Можно добавить всплывающую подсказку если заключить её текст в кавычки в конце скобки с адресом

11)код окружается тремя косыми чертами: ` . После открывающих черточек должен быть указан язык программирования

---

Для клонирования: Зайти в репозиторий в гитхабе, нажать Code, перейти на настройку SSH, скопировать ссылку. Через баш перейти в желаемую папку на своём ПК, сделать её репозиторием (инструкция есть выше) и прописать git clone Скопированный_Адрес (либо адрес страницы. В этом надо разобраться). После можно проверить всё тем же git remote -v

Для форка: нажать форк в репозитории в гитхабе, после он будет доступен по адресу https://github.com/%USERNAME%/git-basics, где %USERNAME% — ваше имя пользователя. После скопировать репозиторий локально 
