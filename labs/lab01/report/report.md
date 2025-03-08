---
## Front matter
title: "Лабораторная работа №1"
subtitle: "курс: Операционны системы"
author: "Байдина Елизавета Дмитриевна"

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

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Задание

Здесь приводится описание задания в соответствии с рекомендациями
методического пособия и выданным вариантом.

# Теоретическое введение

Здесь описываются теоретические аспекты, связанные с выполнением работы.

Например, в табл. [-@tbl:std-dir] приведено краткое описание стандартных каталогов Unix.

: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `/bin `      | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/home`      | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/media`     | Точки монтирования для сменных носителей                                                                                   |
| `/root`      | Домашняя директория пользователя  `root`                                                                                   |
| `/tmp`       | Временные файлы                                                                                                            |
| `/usr`       | Вторичная иерархия для данных пользователя                                                                                 |

Более подробно про Unix см. в [@tanenbaum_book_modern-os_ru; @robbins_book_bash_en; @zarrelli_book_mastering-bash_en; @newham_book_learning-bash_en].

# Выполнение лабораторной работы

Устанавливаем VirtualBox. Создаем виртуальную машину с операционной системой Linux Fedora. (рис. [-@fig:001]).

![Название рисунка](image/1.jpg){#fig:001 width=70%}

Заходим в ОС под заданной при установке учетной записью. Нажимаем комбинацию Win+Enter для запуска терминала. (рис. [-@fig:002]).

![Название рисунка](image/2.jpg){#fig:002 width=70%}

Переключаемся на роль супер-пользователя. (рис. [-@fig:003]).

![Название рисунка](image/3.jpg){#fig:003 width=70%}

Устанавливаем средства разработки. (рис. [-@fig:004]).

![Название рисунка](image/4.jpg){#fig:004 width=70%}

Обновляем все пакеты. (рис. [-@fig:005]).

![Название рисунка](image/5.jpg){#fig:005 width=70%}

Скачиваем программы для удобства работы в консоли. (рис. [-@fig:006]).

![Название рисунка](image/6.jpg){#fig:006 width=70%}

Скачиваем программы для удобства работы в консоли. (рис. [-@fig:007]).

![Название рисунка](image/7.jpg){#fig:007 width=70%}

При необходимости можно использовать автоматическое обновление. Устанавливаем программное обеспечение(рис. [-@fig:008]).

![Название рисунка](image/8.jpg){#fig:008 width=70%}

Запускаем таймер. (рис. [-@fig:009]).

![Название рисунка](image/9.jpg){#fig:009 width=70%}

Так как в данном курсе мы не будем работать с системой безопасности SELinux отключаем её. Для этого в файле /etc/selinux/config заменим значение SELINUX=enforcing на SELINUX=permissive. После этого перезапускаем виртуальную машину. (рис. [-@fig:010]).

![Название рисунка](image/10.jpg){#fig:010 width=70%}

Запускаем терминальный мультиплексор tmux. (рис. [-@fig:011]).

![Название рисунка](image/11.jpg){#fig:011 width=70%}

Создаем конфигурационный файл ~/.config/sway/config.d/95-system-keyboard-config.conf.  (рис. [-@fig:012]).

![Название рисунка](image/12.jpg){#fig:012 width=70%}

Редактируем созданный файл.  (рис. [-@fig:013]).

![Название рисунка](image/13.jpg){#fig:013 width=70%}

Переключаемся на роль супер-пользователя.  (рис. [-@fig:014]).

![Название рисунка](image/14.jpg){#fig:014 width=70%}

Отредактируем конфигурационный файл /etc/X11/xorg.conf.d/00-keyboard.conf с помощью файлого менеджера mc и его втроенного редактора.  (рис. [-@fig:015]).

![Название рисунка](image/15.jpg){#fig:015 width=70%}

Перезапускаем виртуальную машину. (рис. [-@fig:016]).

![Название рисунка](image/16.jpg){#fig:016 width=70%}

Запускаем терминальный мультиплексор tmux. (рис. [-@fig:017]).

![Название рисунка](image/17.jpg){#fig:017 width=70%}

Переключаемся на роль супер-пользователя.  (рис. [-@fig:018]).

![Название рисунка](image/18.jpg){#fig:018 width=70%}

Установите имя хоста. Проверяем выполнение команды. (рис. [-@fig:019]).

![Название рисунка](1image/19.jpg){#fig:020 width=70%}

Устанавливаем pandoc с помощью менеджера пакетов. (рис. [-@fig:020]).

![Название рисунка](image/20.jpg){#fig:022 width=70%}

Устанавливаем дистрибутив TeXlive. (рис. [-@fig:021]).

![Название рисунка](image/21.jpg){#fig:026 width=70%}

# Выводы

Я приобрела практические навыки установки операционной системы на виртуальную машину, научилась делать настройку минимально необходимых для дальнейшей работы сервисов.

# Список литературы{.unnumbered}

::: {#refs}
:::
