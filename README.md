# Laravel_install

---

## Что нужно

- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- [Vagrant](https://www.vagrantup.com/downloads)

## Как установить

1.

Начиная с 13-той версии Homestead перестал поддерживать Virtual Box. Теперб нужно заходить на страницу `https://github.com/laravel/homestead.git` далее в tags и выбирать версию ниже 13-той. Выбрать Source code.zip

Создайте директорию будущей виртуальной машины и закинуть файлы из архива в неё

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

***Убедится что антивирус отключен***

`git checkout release`

`vagrant up --provision`

4.

Зайти на виртуалку через терминал

`vagrant ssh`

Зайти в дирректорию с сайтом 

`cd /home/vagrant/laravel.loc/`

Выполнить команду по установке Laravel с точкой в конце что бы не создавалась дочерняя папка

`composer create-project laravel/laravel .`

для установки конкретной версии laravel `composer create-project laravel/laravel example-app "8.5.*"`

5.

Проверить доступность страницы проекта зайдя на неё по настроенному имени - `laravel.loc/`


---
