# Laravel_install

---

## Что нужно

- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- [Vagrant](https://www.vagrantup.com/downloads)

## Как установить

1.

Создайте директорию будущей виртуальной машины и скачать с помощью GIT репозиторий с Homested - `git clone https://github.com/laravel/homestead.git`

2.

В папке homested выполнить скрипт init.bat

Открыть с помощью VSCode папку homested

Отредактировать файл Homested.yaml, указав путь к папке и имя сайта

```
folders:
    - map: H:\Laravel\porjects\laravel.loc
      to: /home/vagrant/laravel.loc

sites:
    - map: laravel.loc
      to: /home/vagrant/laravel.loc/public      
```

3.

Прописать ip и имя в файле hosts в windows.

4.

Запускать сборку виртуальной машины из терминала VSCode

``Убедится что антивирус отключет``

`git checkout release`

`vagrant up --provision`

4.

Зайти на виртуалку через терминал

`vagrant ssh`

Зайти в дирректорию с сайтом 

`cd /home/vagrant/laravel.loc/`

Выполнить команду по установке Laravel с точкой в конце что бы не создавалась дочерняя папка

`composer create-project laravel/laravel .`

5.

Проверить доступность страницы проекта зайдя на неё по настроенному имени - `laravel.loc/`


---
