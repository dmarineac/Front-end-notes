# [Навыки > ](../teach.md)JavaScript
### Вопросы:
<details>
    <summary>
        Типы данных(https://learn.javascript.ru/types-intro)
    </summary>
    
* nuber(число)
* string(строка)
* boolean(логический)
* null(специальное значение)
* undefined(специальное значение)
* object(объекты)
* promise
</details>

<details>
    <summary>
        Функции
    </summary>
<details>
    <summary>
        Function Expression/Function Declaration
    </summary>
Основное отличие между Function Expression/Declaration: функции, объявленные как Function Declaration, создаются интерпретатором до выполнения кода.Поэтому их можно вызвать до объявления.

    //Function Expression - объявление функции в контексте какого-либо выражения, например присваивания
    var sum = function(a, b) {
      return a + b;
    }
    
    //Function Declaration – функция, объявленная в основном потоке кода
    function sum(a, b) {
      return a + b;
    }

</details>

<details>
    <summary>
        Анонимная фун-ия
    </summary>
Функциональное выражение, которое не записывается в переменную, называют анонимной функцией.
</details>

<details>
    <summary>
        new Function
    </summary>
Метод создания фун-ии полностью «на лету» из строки.Таким образом можно конструировать функцию, код которой неизвестен на момент написания программы, но строка с ним генерируется или подгружается динамически во время её выполнения.

    var sum = new Function('a,b', ' return a+b; ');
    var result = sum(1, 2);
    alert( result ); // 3
</details>

<details>
    <summary>
        Named Function Expression. Именованные функциональные выражения
    </summary>
Специально для работы с рекурсией в JavaScript существует особое расширение функциональных выражений, которое называется «Named Function Expression» (сокращённо NFE) или, по-русски, «именованное функциональное выражение».

    var f = function sayHi(...) { /* тело функции */ };
Имя функционального выражения (sayHi) имеет особый смысл. Оно доступно только изнутри самой функции (f).Кроме того, имя NFE нельзя перезаписать.NFE используется в первую очередь в тех ситуациях, когда функцию нужно передавать в другое место кода или перемещать из одной переменной в другую.Внутреннее имя позволяет функции надёжно обращаться к самой себе, где бы она ни находилась.
</details>
* Фун-ии конструктор
* .call  .apply
</details>

<details>
    <summary>
        В чем отличия между методом и свойством    
    </summary>
Обращение к методу всегда идет со скобками, а к свойству – без скобок.
Обратите внимание, str.length – это свойство строки, а str.charAt(pos) – метод, т.е. функция.
</details>

* Делегирование на захвате
* validity
* Drag(перетаскивание)
    mousedown
    mouseup
* Drag and Drop
* Коллбек(callBack) - фун-ия обратоного вызова - предназначенная для отложенного выполнения
* Single Responsibility Principal (переиспользуемость кода)
* JSONP(JSON with Padding, JSON с набивкой) - способ загрузки данных, основанный на подключение из кода тега script, который вызывает заранее определенную фун-ию.
* работа с массивом 
    мапирование
        перебирающие методы:
            .forEach используется для перебора массива
            .filter используется для фильтрации массива через функцию
            .map используется для трансформации массива
            .every/some методы используются для проверки массива
            .reduce/reduceRight используется для последовательной обработки каждого элемента массива с сохранением промежуточного результата
            
        .reverse
            Метод - меняет порядок эл-ов на обратный.
        .sort()
            Метод sort() сортирует массив на месте.Если не передать функцию сравнения – сортирует элементы как строки.
        .join
        .concat
            Объединяет массивы.
        .split
            Метод split(s), который позволяет превратить строку в массив, разбив ее по разделителю s.
            
            var names = 'Маша, Петя, Марина, Василий';
            var arr = names.split(', ');
            for (var i = 0; i < arr.length; i++) {
              alert( 'Вам сообщение ' + arr[i] );
            }
          
        .splice
            Метод splice – Умеет все: удалять элементы, вставлять элементы, заменять элементы – по очереди и одновременно.
            arr.splice(index[, deleteCount, elem1, ..., elemN])
                Удалить deleteCount элементов, начиная с номера index, а затем вставить elem1, ..., elemN на их место. Возвращает массив из удалённых элементов. 
        .slice
            Метод slice(begin, end) копирует участок массива от begin до end, не включая end.
        .reduce
        Array.from
        push/pop добавление/удаление элемента из конца массива
        shift/unshift добавление/удаление элемента из начала массива
        indexOf/lastIndexOf возвращают позицию элемента в массиве (не поддерживается в IE8-)
        Object.keys(obj) возвращает массив свойств объекта
* Оптимизация
    debounce
    throtling
* FileReader
    base64    
* Узкие места JS    
    
<details>
    <summary>
        Перечисления(Enumeration)
    </summary>
Объект со списком констант

    var Status = {
        OK: 200,
        REDIRECT: 300,
        ERROR: 400,
        SERVER_ERROR: 500
    };
</details>

* Словарь 
* Императивный/Декларативный
* Утинная типизация(Duck Typing)
<details>
    <summary>
        AJAX
    </summary>
    
HTTP
    GET - получить данные и заголовки
    HEAD - получить только заголовки
    POST - отправить(создать несуществующие данные) 
    PUT - положить(изменить существующие данные) 
    DELETE - удалить
    Код состояния:
        1хх - информационное сообщения
        2хх - успешные сообщения
            200 ОК - все хорошо можно продолжать
        3хх - перенаправление
            301 Move Permanently - ресурс переехал на всегда
            307 Temporary Redirect - ресурс переехал временно  
        4хх - ошибка в запросе клиента
            400 Bad Request - неправельный запрос 
            404 Not Found - запрашваемый ресурс не найден
        5хх - ошибки сервера
            500 Internal Server Error - произошла внутреняя(на сервере) ошибка
JSON
    Чем отличается JSON от объекта JS
        - все ключи объявляются в двойных кавычках
        - строки объявлены только в двойных кавычках
        - не может быть фун-ий
XMLHttpRequest - объект для работы с HTTP 

Как сказать о неправильных данных?
 
    return undefined; - просто промолчать и ничего не вернуть из фун-ии
    return NaN; - иметь спец. значение, означающее неправильный параметр и вернуть его
    return [undefined, 'Неправильные данные']; - возвращать всегда пару значений. Результат и сообщение об ошибке
    throw new Error('Неправильные данные'); - использовать спец. механизм исключений
    
    'use strict';
    var xhr = new XMLHttpRequest();
    xhr.addEventListener('load', function () {
       try{
           console.log(JSON.parse(xhr.responseText));
       }catch(err){
           console.error(err.message);
       }
    });
    
    xhr.open('GET', 'http://pathTo/data.json');
    xhr.send();
</details>

<details>
    <summary>
        IIFE.Оператор круглые скобки(для фун-ий)
    </summary>

фун-ия создастся,отработает и исчезнет

    (function(){
        //тело фун-ии
        //переменные созданные внутри фун-ии - локальные
    })();
</details>

<details>
    <summary>
        Модули
    </summary>
Обособленная часть программы, которая может заменяться/использоваться повторно в разных местах программы(или даже нескольких проектах). Или же часть программы решающей узкий набор задач.
</details>

<details>
    <summary>
        DOM(https://learn.javascript.ru/dom-nodes)
    </summary>
`console.log(document.parentElement)`
</details> 
 Замыкание
 event bubbling и какую пользу из него можно извлечь
 разница между Function#bind, Function#apply и Function#call
 разница между стрелочной функцией и обычной
 напишите FizzBuzz
 как работать с массивами, объектами(сортировать, фильтровать, и т.д). как работать c http запросами
 closures, callbacks, fetch, class, promise,  event

<details>
    <summary>
        Передача по значению/по ссылке
    </summary>
</details>

<details>
    <summary>
        Ограничения JS в браузере
    </summary>
    
     * Нельзя взаимодействовать с файловой системой.
     * Нет доступа к сетевым фун-ям, кроме того что предоставляет сам браузер.
     * Нет возможности создавать многопоточные вычисления.
     * Нельзя создавать новые процессы/запускать программы(открытия новых вкладок не считается)
</details>

* Single Responsibility Principal
* Коллбэк(call back)
    Коллбэк(call back - обратный вызов) фун-я обратного вызова - фун-я предназначенная для отложенного выполнения
 События
    DOM Lebel 0 - object.onclick = function(){}
    DOM Lebel 1 - addEventListener
    Другие события
 Таймеры и интервалы
 Способы передачи коллбэка
 * записать коллбэк как св-во объекта или переменную известную фун-ю
 * передать коллбэк параметром

<details>
<summary>Методы работы c DOM(https://learn.javascript.ru/dom-nodes)</summary>
    <details>
        <summary>
            querySelector()   //Метод для поиска элементов(находит первый элемент, если их несколько, проще использовать его - т.к. ищет и по классам и по id).
        </summary>
        
            document.querySelector(".user-block")
            //document  - где будем искать
            //querySelector(".user-block")  - метод для поиска элемента
            //(".user-block)    - что конкретно я ищу
            
            Для того чтобы найти все элементы исп. метод `querySelectorAll`
            
            document.querySelectorAll('nav li')
            
            var link = document.querrySelector(".nameOfYourCssSelector")
</details>
    <details>
        <summary>
            addEventListener()  //Метод для отлова "диких" событий
        </summary>
        
            link.addEventListener('click', function(){});
            //link  - элемент у которого мы будем ловить события
            //addEventListener('click', function(){});  - метод отлова события
            //'click'   - определяем какие [события](https://learn.javascript.ru/introduction-browser-events) мы ловим
            //function(){}  - фун-ия которая будет выполняться каждый раз когды мы ловим событие клик
            
            
            var button = document.getElementById('clickable');
            var buttonClickHandler = function(){    //именуй обработчик события либо Handler или On (var = OnButtonClick )
                alert('Hello from first handler');
            };
            link.addEventListener('click', buttonClickHandler)  //используй фун-ию в методе без скобок
            
</details>
<details>
    <summary>
        classList   //Набор методов для управления классами
    </summary>
    

</details>
<details>
    <summary>
        .removeChild    //удалить DOM ноду
    </summary>
</details>
<details>
        <summary>
            .appendChild         //переместить(вставляется в конец списка, так же можно сортировать) 
        </summary>
</details>
<details>
        <summary>
            .insertBefore   //точечная вставка (переместить в середину)
        </summary>
</details>
<details>
        <summary>
            .replaceChild   //заменить блок
        </summary>
</details>
<details>
        <summary>
            .cloneNode  //скопировать блок
        </summary>
</details>
<details>
        <summary>
            .innerHTML  //возвращает всю разметку
        </summary>
</details>
<details>
        <summary>
            .textContet  //возвращает только текстовое
        </summary>
</details>
</details>

[event.preventDefault();](https://developer.mozilla.org/ru/docs/Web/API/Event/preventDefault)
<details>
    <summary>
        События(Event):
    </summary>
    preventDefault()    //отмена действия по умолчанию
    stopPropagation()   //прекращение распространения
    
Mouse events:
    click, dbclick, keydown, keypress, keyup, mouseover, mouseout

Focus events:
    blur, focus, focusin, focusout, change

Form events:
    reset, submit
</details>

### WebComponents
<details>
        <summary>
            template
        </summary>
</details>

#### classList   //Набор методов для управления классами

    element.classList.add('modal-content-show')
    //element   - елемент которому добавляем новый класс
    //classList - св-во содержащее в себе методы для работы с классами
    //add('modal-content-show') - метод добавления класса
    //'modal-content-show'  - название класса которое нужно добавить элементу

    element.classList.add()         //добавляет класс
    element.classList.remove()      //удаляет класс
    element.classList.toggle()      //переключает класс(если есть класс то он его заменяет )
    element.classList.contains()    //сообщает есть ли класс у элемента
    
    
     

document, window 

### Атрибуты и сво-ва
<details>
    <summary>
        getAttribute(name)
    </summary>
    
`h1.getAttribute('id')      //получить id найденный в заголовке h1
                            //getAttribute(name) - name - регистронезависимый`
</details>
<details>
    <summary>
        setAttribute(name, value)
    </summary>
    

</details>
<details>
    <summary>
        hasAttribute(name)
    </summary>
    

</details>
<details>
    <summary>
        removeAttribute(name)
    </summary>
    

</details>
<details>
    <summary>
        attributes        
    </summary>
    

</details>
### Оптимизация 
<details>
    <summary>
        Измерение скорости работы скрипта(микросекундах)
    </summary>
    
`var time = performance.now();
 // некий код
 time = performance.now() - time;
 console.log('Время выполнения = ', time);`
</details>

* [Повышаем производительность клиентской части веб-приложения](https://xakep.ru/2014/07/22/speedup-client-javascript/)
* [Измерение производительности функций в JavaScript](https://habr.com/ru/company/mailru/blog/272087/)
---
Полезные ссылки:
* [Современный учебник Javascript - Илья Кантор](https://learn.javascript.ru/) 
* [JSGarden](http://bonsaiden.github.io/JavaScript-Garden/ru/)
* [Выразительный JS](https://karmazzin.gitbooks.io/eloquentjavascript_ru/content/index.html)
* [Practical Modern JavaScript - Nicolas Bevacova](https://github.com/mjavascript/practical-modern-javascript)
* [You Don't Know JS - Kyle Simpson](https://github.com/getify/You-Dont-Know-JS), [Почему WAT](https://habr.com/post/137188/)
* [Тестирование знаний по JS](https://learn.javascript.ru/quiz)
* [The Favorit WebApp](https://thefwa.com/)