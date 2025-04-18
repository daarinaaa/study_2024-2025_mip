---
## Front matter
lang: ru-RU
title: Лабораторная работа № 6
subtitle: Модель «хищник–жертва»
author:
  - Шияпова Д.И.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 05 апреля 2025

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


## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Шияпова Дарина Илдаровна
  * Студентка
  * Российский университет дружбы народов
  * [1132226458@pfur.ru](mailto:1132226458@pfur.ru)


:::
::: {.column width="30%"}

![](./image/dishiyapova.jpeg)

:::
::::::::::::::

## Цель работы

Реализовать модель "хищник-жертва" в *xcos*.

## Задание

1. Реализовать модель "хищник-жертва" в xcos;
2. Реализовать модель "хищник-жертва" с помощью блока Modelica в xcos;
3. Реализовать модель "хищник-жертва" в OpenModelica

## Выполнение лабораторной работы

Модель «хищник–жертва» (модель Лотки — Вольтерры) представляет собой модель
межвидовой конкуренции. В математической
форме модель имеет вид:

$$
\begin{cases}
  \dot x = ax - bxy \\
  \dot y = cxy - dy,
\end{cases}
$$

## Выполнение лабораторной работы

![Задание переменных окружения в xcos для модели](image/1.png){#fig:001 width=70%}

## Выполнение лабораторной работы

![Модель «хищник–жертва» в xcos](image/2.png){#fig:002 width=70%}

## Выполнение лабораторной работы

![Задание начальных значений в блоках интегрирования](image/3.png){#fig:003 width=70%}

## Выполнение лабораторной работы

![Динамика изменения численности хищников и жертв модели Лотки-Вольтерры при $a = 2, b = 1, c = 0.3, d = 1, x(0) = 2, y(0) = 1$](image/5.png){#fig:005 width=70%}

## Выполнение лабораторной работы

![Фазовый портрет модели Лотки-Вольтерры при $a = 2, b = 1, c = 0.3, d = 1, x(0) = 2, y(0) = 1$](image/6.png){#fig:006 width=70%}

## Выполнение лабораторной работы

![Модель «хищник–жертва» в xcos с применением блока Modelica](image/7.png){#fig:007 width=70%}

## Выполнение лабораторной работы

![Параметры блока Modelica для модели "хищник–жертва"](image/8.png){#fig:008 width=70%}

## Выполнение лабораторной работы

![Параметры блока Modelica для модели "хищник–жертва"](image/9.png){#fig:009 width=70%}

## Выполнение лабораторной работы

![Динамика изменения численности хищников и жертв модели Лотки-Вольтерры при $a = 2, b = 1, c = 0.3, d = 1, x(0) = 2, y(0) = 1$](image/10.png){#fig:010 width=70%}

## Выполнение лабораторной работы

```
  parameter Real a = 2;
  parameter Real b = 1;
  parameter Real c = 0.3;
  parameter Real d = 1;
  parameter Real x0 = 2;
  parameter Real y0 = 1;

  Real x(start=x0);
  Real y(start=y0);
equation
    der(x) = a*x - b*x*y;
    der(y) = c*x*y - d*y;
```

## Выполнение лабораторной работы

![Динамика изменения численности хищников и жертв модели Лотки-Вольтерры при $a = 2, b = 1, c = 0.3, d = 1, x(0) = 2, y(0) = 1$](image/12.png){#fig:012 width=70%}

## Выводы

В процессе выполнения данной лабораторной реализована модель "хищник-жертва" в *xcos*.
