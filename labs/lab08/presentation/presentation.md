---
## Front matter
lang: ru-RU
title: Лабораторная работа 8
subtitle: Модель TCP/AQM
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

Реализовать модель TCP/AQM с помощью xcos и OpenModelica.

## Задание

- Реализовать в xcos и OpenModelica модель TCP/AQM.
- Построить график, описывающий динамику размера очереди и TCP окна
- Построить фазовый портрет, описывающий зависимость размера очереди от TCP окна

# Выполнение лабораторной работы

## Выполнение лабораторной работы

## Выполнение лабораторной работы

![Переменное окружение](image/1.png){#fig:001 width=70%}

## Выполнение лабораторной работы

![Модель TCP/AQM в xcos](image/2.png){#fig:002 width=70%}

## Выполнение лабораторной работы

![Динамика изменения размера TCP окна W (t) и размера очереди Q(t)](image/3.png){#fig:003 width=70%}

## Выполнение лабораторной работы

![Фазовый портрет (W, Q)](image/4.png){#fig:004 width=70%}

## Выполнение лабораторной работы

![[Динамика изменения размера TCP окна W (t) и размера очереди Q(t) при С = 0.9](image/5.png){#fig:005 width=70%}

## Выполнение лабораторной работы

![Фазовый портрет (W, Q) при С = 0.9](image/6.png){#fig:006 width=70%}

## Выполнение лабораторной работы

![Модель TCP/AQM в OpenModelica](image/7.png){#fig:007 width=70%}

## Выполнение лабораторной работы

![Установки симуляции OpenModelica](image/8.png){#fig:008 width=70%}

## Выполнение лабораторной работы

![Динамика изменения размера TCP окна W (t) и размера очереди Q(t). OpenModelica](image/9.png){#fig:009 width=70%}

## Выполнение лабораторной работы

![Фазовый портрет (W, Q). OpenModelica](image/10.png){#fig:010 width=70%}

## Выводы

В результате выполнения работы была реализована модель $M|M|1|\infty$ с помощью xcos.
