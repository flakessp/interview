# Cписок общих вопросов
- Что такое домен?
- Что такое ip?
- Чем отличается клиент от сервера?
- Что происходит когда мы вбиваем 'google.com' в адресную строку браузера и нажимаем Enter?
- Http запросы 
- Коды ошибок
- Чем отличие куки от сессии
- Токенизация
- Пререндеринг и сервер-рендеринг


- Псевдокод
- Примитивные алгоритмы
- CORS
- Варианты передачи данных с клиента на сервер


# Список вопросов по HTML/CSS
- Чем отличается блочный элемент от линейного?
- Как выровнять элемент (блочный/линейный) по горизонтали?
- А по вертикали?

- Псевдоэлементы
- айфреймы

- Канвас
- Вебаудио / вебжл

# Список вопросов по JS разработчика
- Методы массивов
- Методы объектов
- Методы строк

- Изоляция скоупа
- Call (как вызвать метод массива на строки)

- Ооп (наследование)

- зачем нужны .prototype?

- базовый вопрос на циклы и понимание контекста, каков результат выполнения кода?
```javascript
(function initLoop() {
  function doLoop(x) {
    i = 3;
    console.log('loop:', x);
  }

  for (var i = 0; i < 10; i++) {
    doLoop(i + 1);
  }
})();
```

- понимание контекстов
```javascript
'use strict';

(function () {
  const student = { name: 'James' };

  function createStudent(name) {
    const student = { name: name };
    return student;
  }

  console.log(createStudent('Ken'));
  console.log(student);
})();
```


- в чем разница ?
```javascript
function Dice(sides) {
  this.sides = sides;
}

Dice.prototype.roll = function () {
  var random = Math.floor(Math.random() * this.sides) + 1;
  return random;
}
// от
function Dice(sides) {
  this.sides = sides;
  this.roll = function () {
    var random = Math.floor(Math.random() * this.sides) + 1;
    return random;
  }
}

```

- Замыкания
- Карринг

## Задачи на понимание this и передача контекста
### Перепишите суммирование аргументов
Есть функция sum, которая суммирует все элементы массива:
```javascript
function sum(arr) {
  return arr.reduce(function(a, b) {
    return a + b;
  });
}

alert( sum([1, 2, 3]) ); // 6 (=1+2+3)
```
Создайте аналогичную функцию sumArgs(), которая будет суммировать все свои аргументы:

```javascript
function sumArgs() {
  /* ваш код */
}

alert( sumArgs(1, 2, 3) ); // 6, аргументы переданы через запятую, без массива
```
### Примените функцию к аргументам

Напишите функцию applyAll(func, arg1, arg2...), которая получает функцию func и произвольное количество аргументов.

Она должна вызвать func(arg1, arg2...), то есть передать в func все аргументы, начиная со второго, и возвратить результат.

Например:
```javascript
// Применить Math.max к аргументам 2, -2, 3
alert( applyAll(Math.max, 2, -2, 3) ); // 3

// Применить Math.min к аргументам 2, -2, 3
alert( applyAll(Math.min, 2, -2, 3) ); // -2
```

# Node.js

Что будет результатом выполнения следующего кода?

```javascript
var http = require("http");

http.createServer(function(request, response) {
  response.writeHead(200, {'Content-Type': 'text/plain'});

  setTimeout(function(){
    response.end('Goodbye World\n');
  }, 1000);

  response.write("Hello World\n");
}).listen(3000);
```

Что выведется в консоли?
```javascript
var fs = require("fs");
//readFile по умолчанию выполняется асинхронно
fs.readFile('/etc/this/file/exists.txt', function (err, data) {
  if (err) throw err;
  console.log("File read.");
});

console.log("I love bees.");
```

# React

Как сделать проверку на типы передаваемых значений (props)?
> Component.propTypes = {stringVar:React.PropTypes.string}

Как сделать значения по умолчания в случае отсутсвия данных?
> Component.defaultProps = {stringVar:'default value'}

How should you set an initial state value for a component?

How do we communicate events up through the DOM tree in a standard React application?

How do we define a property called onChange is a required function for a Counter component?


#ES6

Отличие объявления переменных с помощью let/const от var
