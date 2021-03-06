# Вызов не чаще чем в N миллисекунд

[importance 5]

Напишите функцию `debounce(f, ms)`, которая возвращает обёртку, которая передаёт вызов `f` не чаще, чем раз в `ms` миллисекунд.

"Лишние" вызовы игнорируются. Все аргументы и контекст -- передаются.

Например:

```js
//+ no-beautify
function f() { ... }

var f = debounce(f, 1000);

f(1); // выполнится сразу же
f(2); // игнор

setTimeout( function() { f(3) }, 100); // игнор (прошло только 100мс)
setTimeout( function() { f(4) }, 1100); // выполнится
setTimeout( function() { f(5) }, 1500); // игнор
```

Упрощённо можно сказать, что `debounce` возвращает вариант `f`, срабатывающий не чаще чем раз в `ms` миллисекунд.