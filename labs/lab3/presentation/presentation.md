---
## Front matter
lang: ru-RU
title: Лабораторная работа №3
subtitle: Научное программирование
author:
  - Полиенко Анастасия Николаевна
institute:
  - Российский университет дружбы народов, Москва, Россия
  - НПМмд-02-23
date: 19 сентября 2023

## i18n babel
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

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
---


# Введение в работу с Octave

## Цель лабораторной работы

Освоить основы работы с GNU Octave.

## Задачи лабораторной работы

1. Изучить задание векторов и матриц
1. Изучить операции над векторами
1. Изучить операции над матрицами
1. Построить графики функций
1. Сравнить эффективность двух кодов

# Ход лабораторной работы

## Простейшие операции

Для задания векторов и матриц используются [ и ].

![Вектора и матрицы](image/1.png)

## Векторные операции

В Octave можно складывать вектора и умножать их на скаляр, вычислять скалярное и векторное произведение двух векторов и норму вектора.

![Операции с векторами](image/2.png)

## Матричные операции

В Octave можно складывать и перемножать матрицы, умножать их на скаляр и транспонировать, вычислять определитель и обратную матрицу, находить собственные значения и ранг матрицы.

![Операции с матрицами](image/4.png)

## Построение графиков

Графики строятся с помощью функции plot.

![Улучшенный график $y = \sin x$](image/8.png)

## Два графика на одном рисунке

Графики можно добавить на существующую фигуру с пмощью функции hold on.

![Точки х и у на графике](image/12.png)

## Сравнение циклов и векторных операций

Операции с векторами намного эффективнее циклов.

![Сравнение двух кодов](image/18.png)

## Выводы

Изучила основы языка Octave и научилась работе с векторами и графиками.



