"# four-lecture" 
# Array
```
Массив - это объект, который содержит значения (любого типа), не особенно в именованных свойствах/ключах, 
а скорее в численно индексированном положении
В JavaScript массив — это упорядоченный список значений. Каждое значение называется элементом, заданным 
индекс. ... Во-первых, массив может содержать значения смешанных типов.
Массив — это специальная переменная, которая может содержать более одного значения:
```
```js
var arr = [10,"hello",true]; // Массив из трех элементов
arr[2] = "world"; // Значение по индексу рав
```
## ИЗМЕНЕНИЕ ЭЛЕМЕНТОВ В МАССИВЕ
```js
Вы также можете добавлять элементы или изменять элементы, обращаясь к значению индекса
Предположим, массив состоит из двух элементов. Если вы попытаетесь добавить элемент с индексом 3 (четвертый 
), третий элемент будет неопределенным. Например:
```
```js
var fruits = ["Apple","Banana"];
fruits[3]="Orange"
console.log(fruits)
```
## Методы массива
```js
Добавление и удаление элементов в массивах можно выполнять с помощью
метода push() и pop(). Они работают аналогично метод    
push() - Добавляет новые элементы в конец массива
pop() - Удаляет последний элемент из массива
shift() - Удаляет первый элемент из массива
unshift() - Добавляет новые элементы в начало массива
slice() - Создает новый массив из указанного диапазон
splice() - Изменяет элементы массива
sort() - Переставляет элементы массива по возрастани
reverse() - Возвращает массив в обратном порядке
join() - Функция объединения всех элементов массива в
строку через разделитель (по-умолчанию это зап
льский пробел). Если параметр не задан, то
функция использует запятую как разделитель
toString() - Возвращает строковое представлени
компонентов объекта.
pop() 
forEach() 
join()
indexOf()
concat()
find()
shift() 
map() 
includes()
toString()
push()
reduce()
splice()
slice()
filter()
toReversed()
unshift()
toSorted()
```
## pop()
```js
const arr = [10, 25];
arr.pop(); // удаляем последний элемент и возвращаем его значение
console.log(arr); // [10]
// если ничего не передать функции, она вернёт 
undefined
```
## push()
```js
const arr = [];
arr.push('hello'); // добавляем новый элемент в конец массива и возвращаем его индекс
console.log(arr[0]); // hello
```
## shift() 
```js
let arr = [5, 6, 7];
arr.shift(); // удаляет элемент с начала массива и возвращает его значение
console.log(arr); // [6, 7]
```
## unshift()
```js
let arr = [];
arr.unshift('hello'); // добавляем новый элемент в начало массва и возвращаем размер массива после этого действ
console.log(arr); // ["hello"]
console.log(arr.length); // 1
```

## includes()
```js
const array = ['a', 'b'];
array.includes('c');//false
array.includes('b');//true
```

 ## join()
 ```js
 const items = ["one", "two"];
 let joinedItems = items.join(" ");
 console.log(joinedItems); // one two
 const numbers = [43, 6789, 34, 2];
 let numberString = numbers.join("-");
 console.log(numberString); // 43-6789-34-2
 ```
 ## toString()
 ```js
const array = [1,2,3,4,5,'a','b'];

console.log(array.toString()) // '1,2,3,4,5,a,b'
```

 ## indexOf()
 ```js
const fruits = ["apple", "banana", "orange", "mango"];
const index = fruits.indexOf("apple")
console.log(index)
```
## concat()
```js
let arr1 = new Array();
arr1[0]=5;
console.log(arr1);
let arr2=new Array();
arr2[0]=-1;
console.log(arr2);
var resultArray = arr1.concat(arr2);
console.log(resultArray);
// expected output: Array [-1, 5]
```
## splice()
```js
const numbers = ['one', 'two', 'three', 'four']
numbers.splice(2, 1);
console.log(numbers);//['one', 'two', 'four']
```
## slice()
```js
const words = ['spray', 'limit', 'elite', 'exuberant', 'demanding', 'irate']
const result2 = words.slice(0,2)
const result3 = words.slice(2,-2)
const result4 = words.slice(3)
console.log(result2);//['spray', 'limit'];
console.log(result3);//['elite','exuberant'];
console.log(result4);//['exuberant','demanding','irate'];
```
## toReversed()
```js
const array = [1, 2];
array.reverse();//[2, 1]
console.log(array);//[2, 1]
```
## Метод деструктурирования
```js
let a,b,res;
[a,b] = [10,20];
console.log(a)//10;
console.log(b)//20;
[a,b, ...res] = [1,2,3,4,5,6,7,8,9];
console.log(res);//[3,4,5,6,7,8,9];
```
## Метод распространения
```js
function sum(x,y,z) {
    return x+y+z;
}
const namber = [1,2,3];
// console.log(sum(1,2,3))
console.log(sum(...namber));//6
```
## Метод отдыха
```js
function sum (...res){
    return res
}
console.log(sum(1,2,3))
```

# JavaScript array methods callbacks

## forEach()
```js
const array = ['a', 'b'];
array.forEach((element) => {
    console.log(`Элемент: ${element}`);
    });
    // Элемент: a
    // Элемент: b
 ```
 ## map() 
 ```js
const numbers = [4,9,16,25];
const newArr = numbers.map(Math.sqrt)
console.log(newArr) // [ 2, 3, 4, 5 ]

const numbers2 = [65,44,10,5];
const newArr = number.map(result)

function result(num){
     return num*10;
}
console.log(newArr) //[ 650, 440, 100, 50 ]
 ```
 ## reduce()
 ```js
 const arr = [1,2,3]
 function sum (acc, currVal) {
    acc += currVal;
    return acc;
    }
    const totalSum = arr.reduce(sum);// 6
    console.log(`The total is ${totalSum}`);
 ```
 ## find()
```js
const users = [18,20,35,44];
function isAdult(user) {
    return user > 18 
}
console.log(users.find(isAdult));
```
## filter()
```js
let num =[1,2,3]
const result = num.filter((num)=> num>2)//[3]
console.log(result);//[3]
```
## toSorted()
```js
const arr=[10.1,9,11,18,4]
const result = arr.toSorted((a, b)=> a-b)
console.log(result);
console.log(arr);
```


