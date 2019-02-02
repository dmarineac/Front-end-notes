# [Навыки > ](../teach.md) Bower

Bower - менеджер пакетов(jquery, bootstrap,normalize.css и др.)

### Установка:
    npm install -g bower     //установка bower
    npm update -g bower    // обновление bower

### Работа:
    
    bower init     //инициализация bower
    
    bower s названиебиблиотеки          //поиск библиотеки в bower
    bower info названиебиблиотеки          //показывает версии библиотеки
    bower i названиебиблиотеки -S          //установка библиотеки(с сохранением в продакшене - dependicies - без которых проект работать не будет; devDependencies - библиотеки которые нужны только во время разработки)
    bower i названиебиблиотеки -D          //установка библиотеки(с сохранением в devDependencies - библиотеки которые нужны только во время разработки )
    bower uninstall названиебиблиотеки -S          //удаление библиотеки
    
    bower update названиебиблиотеки          //обновление библиотеки(нужно создать файл: bower.json)
    
    bower list          //показать все установленные библиотеки
    bower list --path          //показать полный путь до библиотек
    
Чтобы использовать самые последние версии библиотек, впишите в файле bower.json в версиях библиотек слово "latest". А затем введите в консоль команду bower update
    
    "dependencies": {
       "jquery": "latest",
       "bootstrap": "latest",
       "modernizr": "latest",
       "normalize-css": "latest"

---
Полезные ссылки:
* [Скринкаст от loftblog](https://www.youtube.com/playlist?list=PLY4rE9dstrJwqwHBF4KFMIo9U0HKIR3UP)
* [Bower: зачем фронтенду нужен менеджер пакетов](http://nano.sapegin.ru/all/bower)