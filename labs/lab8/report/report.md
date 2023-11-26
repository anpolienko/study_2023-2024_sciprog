---
## Front matter
title: "Отчёт по лабораторной работе №8"
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

Изучить работу с собственными значениями в GNU Octave.

# Задание

1. Изучить задачу на собственные значения
1. Исследовать марковские цепи

# Выполнение лабораторной работы

1. Найдём собственные значения и собственные векторы для матриц с помощью функции *eig* (рис. @fig:001).

![Собственные значения и векторы](image/1.png){#fig:001 width=60%}

2. Исследуем модель марковской цепи случайного блуждания. Зададим транспонированную матрицу вероятностей переходов и различные начальные векторы. Найдём вектора вероятности через 5 шагов (рис. @fig:002).

![Марковская цепь через 5 шагов](image/2.png){#fig:002 width=60%}

3. Найдём равновесный вектор для марковского процесса (рис. @fig:003)  

![Нахождение равновесного вектора](image/3.png){#fig:003 width=60%}

Проверим, что он действительно равновесный (рис. @fig:004).

![Проверка](image/4.png){#fig:004 width=60%}

# Выводы

Научилась работе со спектром матрицы в Octave.
