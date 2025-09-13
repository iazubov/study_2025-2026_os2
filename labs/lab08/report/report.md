---
## Front matter
title: "Лабораторная работа №8"
subtitle: "Отчет"
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
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Приобретение навыков написания программ с использованием циклов и обработкой
аргументов командной строки.

# Задание

Написать программы с использованием циклов и обработкой аргументов
командной строки.

# Выполнение лабораторной работы


Создаем каталог для программам лабораторной работы № 8 с помощью команды mkdir, перейдем в него и создадим файл lab8-1.asm с помощью команды touch. Откроем файл в Midnight Commander и заполняем его в соответствии с листингом 8.1

![Создаем файл](image/1.png){#fig:001 width=70%}

![Заполняем файл](image/2.png){#fig:002 width=70%}

Создаем исполняемый файл и запускаем его

![Запускаем файл и смотрим на его работу](image/3.png){#fig:003 width=70%}

Снова открываем файл для редактирования и изменяем его 

![Редактируем файл](image/4.png){#fig:004 width=70%}

Создаем исполняемый файл и запускаем его

![Запускаем файл и смотрим на его работу](image/5.png){#fig:005 width=70%}

Регистру ecx присваиваются значения 9 7 5 3 1 - регистр уменьшается на 2.
Число проходов не соответствует числу N, из-за уменьшения на 2.

Снова открываем файл для редактирования и изменяем его, добавив изменение значения регистра в цикле 

![Редактируем файл](image/6.png){#fig:006 width=70%}

Создаем исполняемый файл и запускаем его

![Запускаем файл и смотрим на его работу](image/7.png){#fig:007 width=70%}

Создаем новый файл с помощью команды touch, открываем файл в Midnight Commander и заполняем его в соответствии с листингом 8.2

![Создаем файл](image/8.png){#fig:008 width=70%}

![Заполняем файл](image/9.png){#fig:009 width=70%}

Создаем исполняемый файл и проверяем его работу, вводя разные значения 

![Смотрим, что получается](image/10.png){#fig:010 width=70%}

Программа обрабатывает 3 аргумента

Создаем файл lab8-3.asm, вводим в него текст программы из листинга 8.3

![Создаем файл листинга](image/11.png){#fig:011 width=70%}

![Заполняем файл](image/12.png){#fig:012 width=70%}

Создаем исполняемый файл и запускаем его

![Создаем объектный файл и проверяем работу программы](image/13.png){#fig:013 width=70%}

Изменим программу, чтоб она выводила произведение

![Редактируем файл](image/14.png){#fig:014 width=70%}

Создаем исполнительный файл и запускаем его

![Создаем объектный файл и проверяем работу программы](image/15.png){#fig:015 width=70%}


# Самостоятельная работа

Вариант 13

1) . Напишите программу, которая находит сумму значений функции 𝑓(𝑥) для 𝑥 = 𝑥1,х2, ..., т.е. программа должна выводить значения е 𝑓(𝑥1) + 𝑓(𝑥2) + ... + 𝑓(𝑥𝑛).
Значения 𝑥𝑖 передаются как аргументы. Вид функции 𝑓(𝑥) выбрать из таблицы
8.1 вариантов заданий в соответствии с вариантом, полученным при выполнении
лабораторной работы № 7. Создайте исполняемый файл и проверьте его работу на
нескольких наборах 𝑥 = 𝑥1, 𝑥2, ..., 𝑥𝑛.

Создаем новый файл,открываем его и пишем программу, которая выведет сумму значений, получившихся после решения выражения 12х-7

![Пишем программу](image/16.png){#fig:016 width=70%}

Транслируем файл и смотрим на работу программы

![Смотрим,что все получилось](image/17.png){#fig:017 width=70%}


# Выводы

Мы научились решать программы с использованием циклов и обработкой
аргументов командной строки

