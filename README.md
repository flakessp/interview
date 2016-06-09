# Список вопросов для JS разработчика

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
