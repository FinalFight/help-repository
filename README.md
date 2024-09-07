# help-repository
Записываю сюда основные команды, моменты по созданию репозиториев и варианты верстки текста, которые обязательно мне пригодятся
Для Git-bash
!Стоит помнить, что при помощи стрелок можно передвигаться между последними командами.
1)pwd - показывает текущее местоположение в файлах
2)cd - меняет местоположение. Пишется - cd имя-папки. При пробелах в названии используются "". Можно использовать tab для автозаполнения, вроде написать firs от названия
first-project, и гит дозаполнит сам.
3)ls - выводит содержимое директории. При добавлении -a выводит скрытые файлы.
4)touch - создаёт файл. Желательно писать расширение также.
5)mkdir - создаёт директорию
6)cp - копирует файл. cp что_копируем куда_копируем
7)mv - двигает файл. Синтаксис как у предыдущего cp
8)cat - читает файл. Пишется вместе с называнием
9)rm - удалить файл перманентно. rmdir удаляет пустую директорию, но с -r удаляет директорию с содержимым.
10)git status - выводит состояние репозитория
11)git log даёт список истории коммитов
Для Github
1)Настроить через git-bash хаб при помощи 2 команд: $ git config --global user.name "ваше имя или ник латиницей" |, потом| $ git config --global user.email ваша электронная почта
2)Создать SSH-ключ. Для этого:
2.1)включить гит-баш. В домашней папке написать $ ls -la .ssh/  | если вывод пустой, всё в порядке. В ином случае ключи создавались, их надо удалить если генерировали не вы.
2.2)сгенерировать ключи при помощи одной из 2 комманд: $ ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub" |или| $ ssh-keygen -t rsa -b 4096 -C "электронная почта, к которой привязан ваш аккаунт на GitHub" | можно поставить пароль после этого.
2.3)в гитхабе создать через настройки профиля новый SSH-ключ.
2.4)в гит-баше ввести $ ssh -T git@github.com
3)создать репозиторий на ПК, в баше перейдя в нужную папку в которой мы его создадим и напечатав команду git init
4)переместить в репозиторий файлы и при помощи git add заставить гит понимать что они к нему относятся. При помощи флага --all добавить можно все файлы
5)сделать коммит при помощи git commit. При добавлении -m можно в "" написать комментарии, что очень рекомендуется
6)
