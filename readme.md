## bài 1: Trình bày sự khác biệt giữa ES5 và ES6?
** Khai báo biến **
- ES5 sử dụng var
- ES6 sử dụng  let và const để khai báo biến, với let cho các biến thay đổi và const cho các biến không hoặc rất ít thay đổi.
** Hàm mũi tên **
- ES5:
```js 
function sum(x, y) {
    return x + y;
}; 
```
- ES6:
```js
const sum = (x, y) => x + y;
```
** Nối chuỗi **
- ES5:
```js
var greeting = "Hello, " + name + "!";
```
- ES6:
```js
const greeting = `Hello, ${name}!`;
```
** Destructuring **
- ES5: không hỗ trợ
- ES6:
```js
const [a, b] = [1, 2];
const {name, age} = person;
```
** vòng lặp **
- ES5: Sử dụng for...in để lặp qua các thuộc tính của đối tượng
- ES6: Giới thiệu for...of để lặp qua các phần tử của một iterable (mảng, chuỗi, map, set).
** Modules **
- ES5: Không có hỗ trợ modules native
- ES6: 
```js
// module.js
export const add = (x, y) => x + y;

// main.js
import { add } from './module.js';
```
** Promise **
- ES5: Sử dụng callback để xử lý bất đồng bộ.
- ES6: Sử dụng promise
```js
const promise = new Promise((resolve, reject) => {
    // async operation
});
promise.then(result => {
    // handle result
}).catch(error => {
    // handle error
});
```

