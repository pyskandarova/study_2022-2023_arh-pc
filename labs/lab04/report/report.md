---
## Front matter
title: "Отчёт по лабораторной работе №4"
subtitle: "дисциплина: Архитектура компьютера"
author: "Скандарова Полина Юрьевна"

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
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
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

Освоение процедуры оформления отчетов с помощью легковесного языка разметки Markdown.

# Выполнение лабораторной работы

Для выполнения Лабораторной работы необходимо открыть терминал, перейти в каталог курса сформированный при выполнении лабораторной работы №3, обновить локальный репозиторий, скачав изменения из удаленного репозиторий, перейти в каталог с шаблоном отчета по лабораторной работе № 4 и провести компиляцию шаблона с использованием Makefile. (рис. [-@fig:001])

![Создание файлов report.pdf и report.docx с использованием Makefile.](image/Арх1.jpg){ #fig:001 width=70% }

При успешной компиляции должны сгенерироваться файлы report.pdf и report.docx. (рис. [-@fig:002])

![Проверка генерации файлов.](image/Арх2.jpg){ #fig:002 width=70% }

Далее нужно удалить полученные файлы с использованием Makefile. (рис. [-@fig:003]) (рис. [-@fig:004])

![Команда для удаления сгенерированных файлов.](image/Арх3.jpg){ #fig:003 width=70% }

![Проверка удаления сгенерированных файлов.](image/Арх4.jpg){ #fig:004 width=70% }

Открываю файл report.md c помощью текстового редактора gedit. (рис. [-@fig:005]) (рис. [-@fig:006])

![Команда для открытия файла report.md.](image/Арх5.jpg){ #fig:005 width=70% }

![Структура файла report.md.](image/Арх6.jpg){ #fig:006 width=70% }

Заполняю отчет и скомпилирую отчет с использованием Makefile, после чего проверяю корректность полученных файлов. (рис. [-@fig:007])

![Написание отчёта в report.md.](image/Арх7.jpg){ #fig:007 width=70% }

# Выводы

В ходе лабораторной работы освоена процедура оформления отчетов с помощью легковесного языка разметки Markdown.


