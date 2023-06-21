# Learn ReactJS with TypeScript
## 1. Tuple.
>Trong TypeScript, Tuple là một kiểu dữ liệu cho phép bạn định nghĩa một mảng có số lượng và kiểu dữ liệu cố định cho mỗi phần tử.

Ví dụ, bạn có thể khai báo một Tuple chứa một số nguyên và một chuỗi như sau:
```ts
let person: [string, number] = ['John Doe', 30];
```
## 2.Enum.
>Enum là một kiểu dữ liệu trong TypeScript cho phép bạn định nghĩa một tập hợp các hằng số có tên. Mỗi hằng số trong Enum được gán một giá trị số nguyên tăng dần mặc định.

Ví dụ, chúng ta đã định nghĩa một Enum có tên là Direction với các hằng số North, South, East, và West. Mặc định, North có giá trị 0, South có giá trị 1, East có giá trị 2, và West có giá trị 3. 
```ts
enum Direction {
  North,
  South,
  East,
  West,
}
```
**Chú ý:** Bạn cũng có thể gán giá trị tùy chỉnh cho các hằng số trong Enum ví dụ như sau:
```ts
enum Direction {
  North = "N",
  South = "S",
  East = "E",
  West = "W",
}
```
## 3. Union 
> Union Types cho phép bạn khai báo một biến có thể chứa nhiều kiểu dữ liệu khác nhau. Bạn sử dụng ký hiệu "|" để liệt kê các kiểu dữ liệu.
Ví dụ:
```ts
let variable: string | number;
variable = 'Hello';
variable = 10;
```
## 4. Literal types 
> Literal types trong TypeScript cho phép bạn chỉ định một giá trị cụ thể cho biến hoặc tham số. Điều này có nghĩa là bạn có thể xác định một kiểu dữ liệu chỉ chấp nhận một giá trị cụ thể.
```ts
let statusCode: 200 | 400 | 404;
statusCode = 200; // Hợp lệ
statusCode = 400; // Hợp lệ
// statusCode = 500; // Không hợp lệ, chỉ chấp nhận 200, 400 hoặc 404
```