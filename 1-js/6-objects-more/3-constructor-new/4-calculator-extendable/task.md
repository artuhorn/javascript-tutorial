# Создайте калькулятор

[importance 5]

Напишите конструктор `Calculator`, который создаёт расширяемые объекты-калькуляторы.

Эта задача состоит из двух частей, которые можно решать одна за другой.
<ol>
<li>Первый шаг задачи: вызов `calculate(str)` принимает строку, например "1 + 2", с жёстко заданным форматом "ЧИСЛО операция ЧИСЛО" (по одному пробелу вокруг операции), и возвращает результат. Понимает плюс `+` и минус `-`.

Пример использования:

```js
var calc = new Calculator;

alert( calc.calculate("3 + 7") ); // 10
```

</li>
<li>Второй шаг -- добавить калькулятору метод `addMethod(name, func)`, который учит калькулятор новой операции. Он получает имя операции `name` и функцию от двух аргументов `func(a,b)`, которая должна её реализовывать.

Например, добавим операции умножить `*`, поделить `/` и возвести в степень `**`:

```js
var powerCalc = new Calculator;
powerCalc.addMethod("*", function(a, b) {
  return a * b;
});
powerCalc.addMethod("/", function(a, b) {
  return a / b;
});
powerCalc.addMethod("**", function(a, b) {
  return Math.pow(a, b);
});

var result = powerCalc.calculate("2 ** 3");
alert( result ); // 8
```

</li>
</ol>

<ul>
<li>Поддержка скобок и сложных математических выражений в этой задаче не требуется.</li>
<li>Числа и операции могут состоять из нескольких символов. Между ними ровно один пробел.</li>
<li>Предусмотрите обработку ошибок. Какая она должна быть - решите сами.</li>
</ul>