## bài 1: Trình bày sự khác biệt giữa ES5 và ES6?

**Khai báo biến**
- ES5 sử dụng var
- ES6 sử dụng  let và const để khai báo biến, với let cho các biến thay đổi và const cho các biến không hoặc rất ít thay đổi.
**Hàm mũi tên**
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
**Nối chuỗi**
- ES5:
```js
var greeting = "Hello, " + name + "!";
```
- ES6:
```js
const greeting = `Hello, ${name}!`;
```
**Destructuring**
- ES5: không hỗ trợ
- ES6:
```js
const [a, b] = [1, 2];
const {name, age} = person;
```
**Vòng lặp**
- ES5: Sử dụng for...in để lặp qua các thuộc tính của đối tượng
- ES6: Giới thiệu for...of để lặp qua các phần tử của một iterable (mảng, chuỗi, map, set).
**Modules**
- ES5: Không có hỗ trợ modules native
- ES6: 
```js
// module.js
export const add = (x, y) => x + y;

// main.js
import { add } from './module.js';
```
**Promise**
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

## bài 2: Hãy định nghĩa một Higher-Order Function?
Một Higher-Order Function là một hàm có ít nhất một trong những đặc điểm sau:
1. Nhận một hoặc nhiều hàm khác làm tham số.
2. Trả về một hàm.
Nói cách khác, Higher-Order Function là hàm làm việc với các hàm khác bằng cách nhận chúng làm đối số hoặc trả về chúng.

## bài 3: IIFEs (Immediately Invoked Function Expressions) là gì?
IIFE (Immediately Invoked Function Expression) là một hàm JavaScript được định nghĩa và thực thi ngay lập tức sau khi nó được tạo ra. IIFE thường được sử dụng để tạo ra một phạm vi mới, giúp ẩn biến và hàm khỏi phạm vi toàn cục, ngăn ngừa xung đột biến và giữ cho mã sạch sẽ và tránh được những tác động phụ không mong muốn.
```js
(function(){
    // code bên trong IIFE
})();
```
**Lợi ích của IIFE**
1. Tránh ô nhiễm không gian tên toàn cục:
Biến và hàm bên trong IIFE không bị lộ ra ngoài, tránh được xung đột với các biến và hàm khác.

2. Đóng gói mã:
IIFE giúp đóng gói mã, tạo ra một phạm vi riêng biệt, đặc biệt hữu ích trong các module hoặc khi cần tách biệt các đoạn mã khác nhau.

3. Tạo ra các biến tạm thời:
Có thể tạo ra các biến tạm thời mà không ảnh hưởng đến phạm vi toàn cục hoặc các phần khác của mã.

4. An toàn hơn khi làm việc với các thư viện:
Khi kết hợp nhiều thư viện hoặc plugin khác nhau, IIFE giúp đảm bảo rằng không có xung đột biến và tất cả các thư viện đều hoạt động độc lập.

## bài 4 Sự khác biệt giữa throw Error(‘msg’) so với throw new Error(‘msg’) là gì?
-  throw Error('msg') thực sự là một cách viết không chính xác trong JavaScript.
- Cách viết đúng và chuẩn xác là sử dụng throw new Error('msg'). 
Khi sử dụng throw new Error('msg'), JavaScript sẽ:

1. Tạo một thể hiện mới của đối tượng Error.
2. Đặt thông điệp của đối tượng Error là 'msg'.
3. Ném thể hiện Error này ra ngoài, giúp bạn có thể bắt và xử lý lỗi này trong các khối try...catch.
```js
try {
    throw new Error('This is an error message');
} catch (e) {
    console.log(e.message); // Output: This is an error message
    console.log(e.name); // Output: Error
}
```

## bài 5: Giải thích sự khác biệt giữa “undefined” và “not defined” trong JavaScript?
- undefined: Là giá trị của một biến đã được khai báo nhưng chưa được gán giá trị.
```js
var x;
console.log(x); // undefined
```
- not defined: Là trạng thái của một biến chưa được khai báo trong phạm vi hiện tại, dẫn đến lỗi ReferenceError khi truy cập.
```js
console.log(y); // ReferenceError: y is not defined
```

