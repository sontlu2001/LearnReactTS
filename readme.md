# Learn ReactJS with TypeScript
## 1. Array
Trong TypeScript, bạn có thể khai báo một mảng (array) bằng cách sử dụng cú pháp sau:

```ts
let arrayName: TypeName[] = [];
```
Ở đây, **arrayName** là tên của mảng bạn muốn khai báo, và **TypeName** là kiểu dữ liệu mà mảng chứa. Bạn cũng có thể khởi tạo giá trị ban đầu cho mảng bằng cách cung cấp các phần tử trong cặp ngoặc vuông [].
> Ví dụ, nếu bạn muốn khai báo một mảng chứa các số nguyên, bạn có thể làm như sau:
```ts
let numbers: number[] = [1, 2, 3, 4, 5];
```
## 2. Object
Trong TypeScript, kiểu dữ liệu của object có thể được định nghĩa bằng cách sử dụng TypeScript's type **annotations** hoặc **interfaces**. 
> Ví dụ về cách định nghĩa kiểu dữ liệu cho object trong TypeScript sử dụng **type annotations**
```ts
let person: { name: string, age: number } = {
  name: "John",
  age: 30
};
```
> Ví dụ về cách định nghĩa kiểu dữ liệu cho object trong TypeScript sử dụng **interfaces**
```ts
interface Person {
  name: string;
  age: number;
}

let person: Person = {
  name: "John",
  age: 30
};
```
## 3. Các cách định nghĩa kiểu dữ liệu cho mảng các object.
Nếu bạn muốn khai báo một mảng các object "person" có thuộc tính "name" và "age" có thể thực hiện một trong những cách như sau:
* Sử dụng **Interface**:
```ts
interface Person {
  name: string;
  age: number;
}

let people: Person[] = [
  { name: "John", age: 30 },
  { name: "Alice", age: 25 },
];
```
* Sử dụng **Type Alias**:
```ts
type Person = {
  name: string;
  age: number;
};

let people: Person[] = [
  { name: "John", age: 30 },
  { name: "Alice", age: 25 },
]
```
* Sử dụng **class**:
```ts
class Person {
  constructor(public name: string, public age: number) {}
}

let people: Person[] = [
  new Person("John", 30),
  new Person("Alice", 25),
];
```