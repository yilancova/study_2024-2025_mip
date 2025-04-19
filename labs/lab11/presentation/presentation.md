---
## Front matter
lang: ru-RU
title: Лабораторная работа 11
subtitle: Модель системы массового обслуживания M|M|1
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

Реализовать в CPN Tools модель системы массового обслуживания M|M|1.

## Задание

- Реализовать в CPN Tools модель системы массового обслуживания M|M|1.
- Настроить мониторинг параметров моделируемой системы и нарисовать графики очереди.

# Выполнение лабораторной работы

## Выполнение лабораторной работы

![Декларации модели СМО](image/1.png){#fig:001 width=50%}

## Выполнение лабораторной работы

![Декларации модели СМО](image/2.png){#fig:002 width=50%}

## Выполнение лабораторной работы

![Граф и параметры сети системы обработки заявок в очереди](image/3.png){#fig:003 width=50%}

## Выполнение лабораторной работы

![Граф и параметры генератора заявок системы](image/4.png){#fig:004 width=50%}

## Выполнение лабораторной работы

![Граф и параметры процесса обработки заявок на сервере системы](image/5.png){#fig:005 width=50%}

## Выполнение лабораторной работы

![Функция Predicate монитора Ostanovka и функция Observer монитора Queue Delay](image/6.png){#fig:006 width=50%}

## Выполнение лабораторной работы

![log файл Queue_Delay](image/7.png){#fig:007 width=35%}

## Выполнение лабораторной работы

![График изменения задержки в очереди](image/8.png){#fig:008 width=50%}

## Выполнение лабораторной работы

![Функция Observer монитора Queue Delay Real](image/9.png){#fig:009 width=50%}

## Выполнение лабораторной работы

![Содержимое Queue_Delay_Real.log](image/10.png){#fig:010 width=25%}

## Выполнение лабораторной работы

![Функция Observer монитора Long Delay Time](image/11.png){#fig:011 width=60%}

## Выполнение лабораторной работы

![Периоды времени, когда значения задержки в очереди превышали заданное значение](image/12.png){#fig:012 width=50%}

## Выводы

В результате выполнения работы была реализована в CPN Tools модель системы массового обслуживания M|M|1.
