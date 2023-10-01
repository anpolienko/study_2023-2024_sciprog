---
## Front matter
title: "Отчёт по лабораторной работе №3"
subtitle: "Дисциплина: Научное программирование"
author: "Полиенко Анастасия Николаевна, НПМмд-02-23"

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
#lot: true # List of tables
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

Освоить основы работы с GNU Octave.

# Задание

1. Изучить задание векторов и матриц
1. Изучить операции над векторами
1. Изучить операции над матрицами
1. Построить графики функций
1. Сравнить эффективность двух кодов

# Выполнение лабораторной работы

## Простейшие операции

Для ведения журналирования используется операция *diary on*. Консоль в Octave можно использовать как простой калькулятор для простейших вычислений.

Для задания векторов и матриц используются [ и ] (рис. @fig:001).

![Вектора и матрицы](image/1.png){#fig:001 width=60%}

## Операции с векторами

1. В Octave можно складывать вектора и умножать их на скаляр, вычислять скалярное и векторное произведение двух векторов и норму вектора (рис. @fig:002).

![Операции с векторами](image/2.png){#fig:002 width=60%}

1. Для вычисления проекции вектора используется формула $proj_{\vec{u}} = \frac{\vec{u} \cdot \vec{v}}{\| \vec{u} \|^2} \vec{v}$ (рис. @fig:003).

![Проекция](image/3.png){#fig:003 width=70%}

## Матричные операции

В Octave можно складывать и перемножать матрицы, умножать их на скаляр и транспонировать, вычислять определитель и обратную матрицу, находить собственные значения и ранг матрицы (рис. @fig:004).

![Операции с матрицами](image/4.png){#fig:004 width=60%}

## Построение простейших графиков

1. Построим график функции $\sin x$ на интеравале $[0, 2\pi]$

Создаём вектор значений $x$ и вектор значений $y$ (рис. @fig:005) и строим простейший график с помощью команды $plot$ (рис. @fig:006).

![Вектора х и у](image/5.png){#fig:005 width=60%}

![График $y = \sin x$](image/6.png){#fig:006 width=70%}

1. Улучшаем график, изменяя цвет и толщину линии, подписывая оси и подгоняя их диапозон, добавляя сетку, легенду и название графика (рис. @fig:007).

![Настройка графика](image/7.png){#fig:007 width=70%}

В результате получаем такой график (рис. @fig:008).

![Улучшенный график $y = \sin x$](image/8.png){#fig:008 width=70%}

1. Построим несколько графиков на одной картинке.

Создаём точки $x$ и $y$ (рис. @fig:009).

![Точки х и у](image/9.png){#fig:009 width=70%}

Выведем их на график (рис. @fig:010).

![Точки х и у на графике](image/10.png){#fig:010 width=70%}

Добавим функцию регрессии и добавим её на существующий график с помощью функции *hold on* (рис. @fig:011).

![Добавление функции регрессии](image/11.png){#fig:011 width=70%}

В результате получаем такой график (рис. @fig:012).

![Результирующий график](image/12.png){#fig:012 width=70%}

1. При построении графиков важно использовать поэлементное, а не матричное умножение.

Создаём вектор значений $x$ (рис. @fig:013).

![Вектор х](image/13.png){#fig:013 width=60%}

При попытке построить график возникает ошибка (рис. @fig:014).

![Попытка построить график](image/14.png){#fig:014 width=70%}

Исправляем матричное умножение на поэлементное, получаем график (рис. @fig:015).

![График $y = x^2 \sin x$](image/15.png){#fig:015 width=70%}

## Сравнение циклов и операций с векторами

Подсчитаем сумму $\sum\limits_1^{100000} \frac{1}{n^2}$.

Это можно сделать с помощью цикла *for* (рис. @fig:016).

![loop_for](image/16.png){#fig:016 width=70%}

Или операции *sum* для вектором (рис. @fig:017).

![loop_vec](image/17.png){#fig:017 width=70%}

Операции с векторами намного эффективнее циклов (рис. @fig:018).

![Сравнение двух кодов](image/18.png){#fig:018 width=70%}

# Выводы

Изучила основы языка Octave и научилась работе с векторами и графиками.
