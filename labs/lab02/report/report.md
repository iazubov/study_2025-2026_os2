---
## Front matter
title: "Лабораторная работа №2"
subtitle: "Отчёт"
author: "Зубов Иван Александрович"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Получить представление о работе с учётными записями пользователей и группами
пользователей в операционной системе типа Linux.

# Задание

1. Прочитайте справочное описание man по командам ls, whoami, id, groups, su, sudo,
passwd, vi, visudo, useradd, usermod, userdel, groupadd, groupdel.
Кулябов Д. С., Королькова А. В. Основы администрирования операционных систем 23
2. Выполните действия по переключению между учётными записями пользователей, по
управлению учётными записями пользователей (раздел 2.4.1).
3. Выполните действия по созданию пользователей и управлению их учётными записями
(раздел 2.4.2).
4. Выполните действия по работе с группами пользователей (раздел 2.4.3).

# Выполнение лабораторной работы

Определим, какую учётную запись пользователя вы используете, введя команду whoami.
Посмотрим более подробную информацию с помощью команды id

![Команды whoami и id](image/1.png){#fig-001 width=70%}

Создадим пользователя alice и зададим ей пароль,тоже самое проделываем с пользователем bob

![Alice and Bob](image/2.png){#fig-002 width=70%}

Откроем файл конфигурации /etc/login.defs для редактирования, используя vim 
Изменим несколько параметров. Например, найдим параметр
CREATE_HOME
и убедимся, что он установлен в значение yes. Также установите параметр
USERGROUPS_ENAB no

![Редактируем файл](image/3.png){#fig-003 width=70%}

Дальше созданим каталоги Pictures,Documents. Изменим содержание файла .bashrc

![Редактируем](image/4.png){#fig-004 width=70%}

Переходим в режим Alice,создаем пользователя carol и меняем его  информацию

 ![Создание нового пользователя](image/5.png){#fig-005 width=70%}

В этом упражнении требуется создать две группы и добавить некоторых пользователей в эти группы.Создаем две группы и добавляем туда пользователей

![Работа с группами](image/6.png){#fig-006 width=70%}

# Выводы

Я получил представление о работе с учётными записями пользователей и группами пользователей в операционной системе типа Linux.

