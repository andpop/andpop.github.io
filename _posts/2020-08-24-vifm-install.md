---
layout: post
title:  "Установка vifm из исходников"
categories: Утилиты
tags: vifm
author: andpop
---

* content
{:toc}

Самую свежую версию vifm можно установить из исходников на официальном сайте [ https://vifm.info/downloads.shtml ](https://vifm.info/downloads.shtml):
* Скачиваем с этой страницы tar.bz2-архив с исходниками.
* Раскрываем архив, запускаем консоль в каталоге с исходниками.
* Если в системе не установлена библиотека libncursesw5, устанавливаем ее: `sudo apt-get install libncursesw5-dev`
* Компилируем и устанавливем программу командами:
``` bash
./configure
make
sudo make install
```

Запускается командой `vifm`.
