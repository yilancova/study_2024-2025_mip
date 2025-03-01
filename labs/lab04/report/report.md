---
## Front matter
title: "Лабораторная работа 4"
subtitle: "Задание для самостоятельного выполнения"
author: "Ланцова Яна Игоревна"

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
lot: false # List of tables
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

Выполнить задание для самостоятельного выполнения.

# Задание

1. Для приведённой схемы разработать имитационную модель в пакете NS-2;
2. Построить график изменения размера окна TCP (в Xgraph и в GNUPlot);
3. Построить график изменения длины очереди и средней длины очереди на первом
маршрутизаторе;
4. Оформить отчёт о выполненной работе.

# Описание моделируемой сети

Описание моделируемой сети:

- сеть состоит из N TCP-источников, N TCP-приёмников, двух маршрутизаторов R1 и R2 между источниками и приёмниками (N — не менее 20);
- между TCP-источниками и первым маршрутизатором установлены дуплексные соединения с пропускной способностью 100 Мбит/с и задержкой 20 мс очередью типа DropTail;
- между TCP-приёмниками и вторым маршрутизатором установлены дуплексные соединения с пропускной способностью 100 Мбит/с и задержкой 20 мс очередью типа DropTail;
- между маршрутизаторами установлено симплексное соединение (R1–R2) с пропускной способностью 20 Мбит/с и задержкой 15 мс очередью типа RED, размером буфера 300 пакетов; в обратную сторону - симплексное соединение (R2–R1) с пропускной способностью 15 Мбит/с и задержкой 20 мс очередью типа DropTail;
- данные передаются по протоколу FTP поверх TCPReno;
- параметры алгоритма RED: qmin = 75, qmax = 150, qw = 0, 002, pmax = 0.1;
- максимальный размер TCP-окна 32; размер передаваемого пакета 500 байт; время моделирования -- не менее 20 единиц модельного времени.

# Выполнение лабораторной работы

Откроем файл .tcl на редактирование, в нем построим сеть. Зададим N = 40 TCP-источников, N = 40 TCP-приёмников, два маршрутизатора r1 и r2 между источниками и приёмниками. Между TCP-источниками и первым маршрутизатором установим дуплексные соединения с пропускной способностью 100 Мбит/с и задержкой 20 мс очередью типа DropTail; между TCP-приёмниками и вторым маршрутизатором установлены дуплексные соединения с пропускной способностью 100 Мбит/с и задержкой 20 мс очередью типа DropTail; между маршрутизаторами установлено симплексное соединение (R1–R2) с пропускной способностью 20 Мбит/с и задержкой 15 мс очередью типа RED, размером буфера 300 пакетов; в обратную сторону - симплексное соединение (R2–R1) с пропускной способностью 15 Мбит/с и задержкой 20 мс очередью типа DropTail. Данные передаются по протоколу FTP поверх TCPReno. Зададим также параметры алгоритма RED: qmin = 75, qmax = 150, qw = 0, 002, pmax = 0.1. Также нам нужно выполнить мониторинг окна TCP и мониторинг очереди. Программа выглядит следующим образом: (рис. [-@fig:001] - [-@fig:003]).

![код программы](image/1.png){#fig:001 width=70%}

![код программы](image/2.png){#fig:002 width=70%}

![код программы](image/3.png){#fig:003 width=70%}

Сеть имеет вид (рис. [-@fig:004]).

![схема сети](image/4.png){#fig:004 width=70%}

В результате получим следующие графики (рис. [-@fig:005] - [-@fig:007]).

![Изменение размера длины очереди на линке (R1–R2) при N=40](image/5.png){#fig:005 width=70%}

![Изменение размера окна TCP на всех источниках при N=40](image/6.png){#fig:006 width=70%}

![Изменение размера средней длины очереди на линке (R1–R2) при N=40](image/7.png){#fig:007 width=70%}

Напишем программу для построения графиков в GNUPlot: (рис. [-@fig:008] - [-@fig:009]).

![код программы](image/8.png){#fig:008 width=70%}

![код программы](image/9.png){#fig:009 width=70%}

Сделаем исполняемым и запустим его. Получим 4 графика. (рис. [-@fig:010] - [-@fig:013]).

![Изменение размера средней длины очереди на линке (R1–R2) при N=40](image/10.png){#fig:010 width=70%}

![Изменение размера длины очереди на линке (R1–R2) при N=40](image/11.png){#fig:011 width=70%}

![Изменение размера окна TCP на линке 1-го источника при N=40](image/12.png){#fig:012 width=70%}

![Изменение размера окна TCP на всех источниках при N=40](image/13.png){#fig:013 width=70%}

# Выводы

В результате выполнения работы была разработана имитационная модель в пакете NS-2 и построены график изменения размера окна и TCP и график изменения длины очереди и средней длины очереди на первом маршрутизаторе (в Xgraph и в GNUPlot).
