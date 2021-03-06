## Содержание

1. [Переменные](#переменные)
    - [Локальные переменные](#локальные-переменные)
    - [Глобальные переменные](#глобальные-переменные)
1. [Оператор сравнения](#оператор-сравнения)
1. [Замена new Object](#замена-new-object)
1. [Точка с запятой](#точка-с-запятой)
1. [Размещение скрипта](#размещение-скрипта)
1. [Завершение Switch](#завершение-switch)
1. [Объявление объектов](#объявление-объектов)
1. [Кавычки](#кавычки)
    - [Помещение в кавычки](#помещение-в-кавычки)
    - [Типы кавычек](#типы-кавычек)


## Переменные

## Локальные переменные

Локальные и постоянные переменные всегда нужно объявлять с помощью let или const. Отсутствие объявления со стороны человека будет компенсировано автоматическим объявлением переменной свойством объекта window, что сделает ее глобальной.

**Хорошо**
```
let x = 12;
```

**Плохо**
```
x = 12;
```

*[К содержанию](#содержание)*


## Глобальные переменные

Следует избегать глобальных переменных, так как они могут изменять объект window, будучи его свойством, а также их легко переписать в любой части кода.

**Пример**
```
const log = () => {
  console.log(x);
}
log(); // Получим undefined
let x = 5;
log(); // Получим 5
```

*[К содержанию](#содержание)*


## Оператор сравнения

При сравнении двух переменных используйте `===`, заместо `==`, который является оператором присвоения.

**Хорошо**
```
0 === 12        // false
"Car" === true  // false
10 === 10       // true
```

**Плохо**
```
0 == 12         // true
"Car" == true   // true
10 == 10        // true
```

*[К содержанию](#содержание)*


## Замена new Object

Написание new Object в объявлении переменных- лишнее действие. Следует использовать разные типы скобок, заместо разных 'новых переменных':
```
          {}  -  new Object()
           0  -  new Number()
       false  -  new Boolean()
          []  -  new Array()
        /()/  -  new RegExp()
function(){}  -  new Function()
```

*[К содержанию](#содержание)*


## Точка с запятой

В конце каждого выражения должна стоять точка с запятой, объявляющая завершение этого выражения.

**Хорошо**
```
let x = 12;
```

**Плохо**
```
let x = 12;
```

*[К содержанию](#содержание)*


## Размещение скрипта

Скрипты стоит располагать в конце тега <body> для более быстрой загрузки страницы.
    
## Завершение Switch

Для предотвращения отсутствия отклика свитча, следует завершать свитч расширением default.
	
**Хорошо**
```
switch (a) { case 1: alert(ответ); default: alert(Тоже ответ);}
```
	
**Плохо**
```
switch (a) { case 1: alert(ответ); case 2: alert(Еще ответ); break;}
```
	
*[К содержанию](#содержание)*
	
	
## Объявление объектов
	
Следует объявлять переменные вверху скрипта, для чистого кода и предотвращения написания функции с переменной, которая объявлена позже.
	
*[К содержанию](#содержание)*
	
	
## Кавычки
	
## Помещение в кавычки
	
Стоит помещать в кавычки только недопустимые идентификаторы, чтобы облегчить оптимизацию JS-Движков.
	
**Пример**
```
let item = {
	a: 1;
	b: 2;
	'c': 3;
};
```
	
*[К содержанию](#содержание)*
	
	
## Типы кавычек
	
Всегда в коде скрипта используйте одинарные кавычки (`''`), если не требуется иного. Двойные ковычки приемлимы только при необходимости использования апострофа (`'`) или одинарной кавычки для других целей.

**Хорошо**
```
var string = 'строка';
var word = "you're";
```
  
**Плохо**
```
var string = "строка";
```
  
*[К содержанию](#содержание)*
