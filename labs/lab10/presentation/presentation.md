---
## Front matter
lang: ru-RU
title: Лабораторная работа 10
subtitle: Задача об обедающих мудрецах
author:
  - Ланцова Я. И.
institute:
  - Российский университет дружбы народов, Москва, Россия

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - \usepackage{fontspec}
 - \usepackage{polyglossia}
 - \setmainlanguage{russian}
 - \setotherlanguage{english}
 - \newfontfamily\cyrillicfont{Arial}
 - \newfontfamily\cyrillicfontsf{Arial}
 - \newfontfamily\cyrillicfonttt{Arial}
 - \setmainfont{Arial}
 - \setsansfont{Arial}
---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Ланцова Яна Игоревна
  * студентка
  * Российский университет дружбы народов

:::
::::::::::::::

## Цель работы

Реализовать в CPN Tools задачу об обедающих мудрецах.

## Задание

- Реализовать в CPN Tools задачу об обедающих мудрецах.
- Вычислить пространство состояний, сформировать отчет о нем и построить граф.

# Выполнение лабораторной работы

## Выполнение лабораторной работы

Начальные данные:
- позиции: мудрец размышляет (dumaet), мудрец ест (est) палочки находятся на столе (sticks on the table)
- переходы: взять палочки (take sticks), положить палочки (put sticks)

## Выполнение лабораторной работы

![Модель задачи об обедающих мудрецах](image/1.png){#fig:001 width=50%}

## Выполнение лабораторной работы

![Задание деклараций задачи об обедающих мудрецах](image/2.png){#fig:002 width=70%}

## Выполнение лабораторной работы

![Запуск модели задачи об обедающих мудрецах](image/3.png){#fig:003 width=50%}

## Выполнение лабораторной работы

![Пространство состояний для модели задачи об обедающих мудрецах](image/4.png){#fig:004 width=70%}

## Выполнение лабораторной работы

![Отчет пространства состояний](image/5.png){#fig:005 width=50%}

## Выводы

В результате выполнения работы была реализована в CPN Tools задача об обедающих мудрецах.
