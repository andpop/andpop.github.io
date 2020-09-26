---
layout: post
title:  "Установка vifm из исходников"
categories: Утилиты
tags: vifm
author: andpop
---

* content
{:toc}
Процедура установки двухпанельного файлового менеджера vifm.


### Установка с официального сайта
Установка с сайта [ https://vifm.info/downloads.shtml ](https://vifm.info/downloads.shtml):
* Скачиваем с этой страницы tar.bz2-архив с исходниками.
* Раскрываем архив, запускаем консоль в каталоге с исходниками.
* Если в системе не установлена библиотека libncursesw5, устанавливаем ее: `sudo apt-get install libncursesw5-dev`
* Компилируем и устанавливем программу командами:
``` bash
./configure
make
sudo make install
```

### Установка из репозитория проекта на GitHub
Также можно установить из репозитория GitHub. Скрипт для установки:
```bash
#!/bin/sh

mkdir vifm_source
cd vifm_source
git clone https://github.com/vifm/vifm.git .
sudo apt-get install -y libncursesw5-dev
./configure
make
sudo make install
cd ..
rm -rf vifm_source
```

Запуск установленной утилиты - команда `vifm`.
