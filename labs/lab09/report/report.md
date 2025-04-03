---
## Front matter
title: "Лабораторная работа №9"
subtitle: "Модель «Накорми студентов»"
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

Реализовать в CPN Tools модель "Накорми студентов".

# Задание

- Реализовать в CPN Tools модель "Накорми студентов".
- Вычислить пространство состояний, сформировать отчет о нем и построить граф.

# Выполнение лабораторной работы

Задаем тип STUD фишкам, относящимся к студентам, тип FOOD - фишкам, относящимся к пирогам, задаём значения переменных x и y для дуг и начальные значения мультимножеств stud_init и food_init (рис. [-@fig:001]).

![Декларации модели «Накорми студентов»](image/1.png){#fig:001 width=70%}

В нашей модели:
- два типа фишек: «пироги» и «студенты»;
- три позиции: «голодный студент», «пирожки», «сытый студент»;
- один переход: «съесть пирожок».

Рисуем граф сети. Для этого с помощью контекстного меню создаём новую сеть, добавляем позиции, переход и дуги(рис. [-@fig:002]):

![Модель «Накорми студентов»](image/2.png){#fig:002 width=70%}

После запуска фишки типа «пирожки» из позиции «еда» и фишки типа «студенты» из позиции «голодный студент», пройдя через переход «кушать», попадают в позицию «сытый студент» и преобразуются в тип «студенты» (рис. [-@fig:003]):

![Запуск модели «Накорми студентов»](image/3.png){#fig:003 width=70%}

Сформируем граф пространства состояний, всего их 4(рис. [-@fig:004]):

![Пространство состояний для модели «Накорми студентов»](image/4.png){#fig:004 width=70%}

Затем сформируем отчет (рис. [-@fig:005]) пространства состояний. Из него может увидеть:

- В графе 4 узла и 3 дуги, соответственно 4 состояния и 3 перехода.
- Затем указаны границы значений для каждого элемента: голодные студенты (максимум - 3, минимум - 0), сытые студенты (максимум - 3, минимум - 0), еда (максимум - 5, минимум - 2, минимальное значение 2, так как в конце симуляции остаются пирожки).
- Также указаны границы мультимножеств.
- Маркировка home равная 4, так как в эту позицию мы можем попасть из любой другой маркировки.
- Маркировка dead равная 4, так как из неё переходов быть не может.
- В конце указано, что нет бесконечных последовательностей вхождений.

![Отчет пространства состояний](image/5.png){#fig:005 width=70%}

# Выводы

В результате выполнения работы была реализована в CPN Tools модель "Накорми студентов".
