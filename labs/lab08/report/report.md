---
## Front matter
title: "Лабораторная работа №8"
subtitle: "Архитектура компьютеров"
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

Изучение команд условного и безусловного переходов. Приобретение навыков написания программ с использованием переходов. Знакомство с назначением и структурой файла листинга.

# Выполнение лабораторной работы

Для начала необходимо создать каталог для программ лабораторной работы № 8, перейти в него и создать файл lab8-1.asm. (рис. [-@fig:001])

![Создание файла в нужной папке](image/Arkh1.png){ #fig:001 width=70% }

Инструкция jmp в NASM используется для реализации безусловных пере-
ходов. Чтобы рассмотреть пример программы с использованием инструкции jmp ввожу в файл lab8-1.asm текст программы из листинга. (рис. [-@fig:002])

![Текст листинга в файле](image/Arkh2.png){ #fig:002 width=70% }

Создаю исполняемый файл и запускаю его. Результат работы данной программы получился следующим. (рис. [-@fig:003])

![Компилляция и запуск программы](image/Arkh3.png){ #fig:003 width=70% }

Изменяю программу таким образом, чтобы она выводила сначала
‘Сообщение № 2’, потом ‘Сообщение № 1’ и завершала работу. Для этого нужно в текст программы после вывода сообщения № 2 добавить инструкцию jmp с меткой _label1 (т.е. переход к инструкциям вывода сообщения № 1) и после вывода сообщения № 1 добавлить инструкцию jmp с меткой _end (т.е. переход к инструкции call quit). Изменяю текст программы в соответствии с листингом. (рис. [-@fig:004])

![Текст листинга в файле](image/Arkh4.png){ #fig:004 width=70% }

Создаю исполняемый файл и проверяю его работу. (рис. [-@fig:005])

![Компилляция и запуск программы](image/Arkh5.png){ #fig:005 width=70% }

Дальше изменяю текст программы изменив и добавив инструкции jmp, чтобы вывод программы был "Сообщение №3", потом "Сообщение №2", потом "Сообщение №1". (рис. [-@fig:006])

![Изменение текста листинга в файле](image/Arkh6.png){ #fig:006 width=70% }

После чего запускаю. (рис. [-@fig:007])

![Компилляция и запуск программы](image/Arkh7.png){ #fig:007 width=70% }

Создаю файл lab8-2.asm в каталоге ~/work/arch-pc/lab08. Внимательно
изучаю текст программы из листинга и ввожу в lab8-2.asm. (рис. [-@fig:008])

![Текст листинга в файле](image/Arkh8.png){ #fig:008 width=70% }

Создаю исполняемый файл и проверяю его работу для разных значений B. (рис. [-@fig:009])

![Компилляция и запуск программы](image/Arkh20.png){ #fig:009 width=70% }

# Изучение структуры файлы листинга

Создаю файл листинга для программы из файла lab8-2.asm и открываю файл листинга lab8-2.lst с помощью текстового редактора mcedit. (рис. [-@fig:010])

![Листинг программы lab8-2](image/Arkh9.png){ #fig:010 width=70% }

Внимательно ознакомившись с его форматом и содержимым, представляю объяснение некоторых строк:
В сторке 29 "00000122" является её адресом, а "7F0C" - машинным кодом инструкции "jg". (рис. [-@fig:011])

![Строка 29](image/Arkh21.png){ #fig:011 width=70% }

В строках 28 и 39 адресами являются "0000011C" и "00000145" соответственно, а кодом инструкции "cmp" - "3P0D". (рис. [-@fig:012])

![Строка 28](image/Arkh23.png){ #fig:012 width=70% }

   

(рис. [-@fig:013])

![Строка 39](image/Arkh22.png){ #fig:013 width=70% }

"39000000" в строке 28 и "0A000000" в строке 39 являются адресами переменных C и B соответственно. (рис. [-@fig:014])

![Адрес переменной С](image/Arkh25.png){ #fig:014 width=70% }

(рис. [-@fig:015])

![Адрес переменной В](image/Arkh24.png){ #fig:015 width=70% }

Далее открываю файл с программой lab8-2.asm и в инструкции с двумя операндами удаляю один операнд. Выполняю трансляцию с получением файла листинга. В этом случае создаётся только сам файл листинга. (рис. [-@fig:016])

![Созданный файл](image/Arkh13.png){ #fig:016 width=70% }

В самом листинге появляется строка об ошибке. (рис. [-@fig:017])

![Строка об ошибке в листинге](image/Arkh12.png){ #fig:017 width=70% }

# Задание для самостоятельной работы

Программа нахождения наименьшей из 3 целочисленных переменных a,b и c. (рис. [-@fig:018])

![Текст программы](image/Arkh16.png){ #fig:018 width=70% }

(рис. [-@fig:019])

![Её компилляция и выполнение](image/Arkh17.png){ #fig:019 width=70% }

Программа для формулы по моему варианту (x+4 при x<4 и ax при x>=4). (рис. [-@fig:020])

![Текст программы](image/Arkh18.png){ #fig:020 width=70% }

(рис. [-@fig:021])

![Её компилляция и выполнение](image/Arkh18.png){ #fig:021 width=70% }

# Выводы

В ходе лабораторной работы изучены команды условного и безусловного переходов. Приобретены навыки написания программ с использованием переходов. Знакомство с назначением и структурой файла листинга прошло успешно.

