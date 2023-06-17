# Learn ReactJS with TypeScript
## 1. Tại sao phải sử dụng TypeScript thay vì JavaScript ?
Xét đoạn code sau:
```ts
function sum(a,b){
    return a +b 
}
console.log(sum('5','4')); //54
```
>Đoạn mã trên đang định nghĩa một hàm **sum(a, b)** nhận vào hai tham số **a** và **b**. Hàm này trả về tổng của hai tham số đó bằng cách sử dụng toán tử '+'.Trong dòng code **console.log(sum('5', '4'));**, hàm sum được gọi với hai tham số là **'5'** và **'4'**. Tuy nhiên, điều không chính xác ở đây là các tham số đang được truyền dưới dạng chuỗi (string) thay vì dạng số. Trong JavaScript, toán tử **'+'** khi được áp dụng cho hai chuỗi sẽ thực hiện phép nối chuỗi, chứ không phải phép cộng số.Vì vậy, kết quả khi in ra màn hình thông qua console.log sẽ là **chuỗi '54'** thay vì **số 9**.

Trong TypeScript, bạn có thể sử dụng kiểu dữ liệu để xác định rõ ràng các loại dữ liệu và tránh các lỗi như trường hợp trên. Trong trường hợp này, bạn có thể sử dụng các kiểu dữ liệu **nguyên thủy (primitives types)** như number để xác định rằng a và b là các số nguyên, chứ không phải chuỗi.

Dưới đây là cách bạn có thể cải thiện đoạn mã trên bằng cách sử dụng kiểu dữ liệu trong TypeScript:
```ts
function sum(a: number, b: number): number {
  return a + b;
}

console.log(sum(5, 4)); // 9
```
## 2. Các primitives types trong TypeScript.
>Trong TypeScript, có một số kiểu dữ liệu nguyên thủy (primitives types) được tích hợp sẵn.Các primitives types trong TypeScript giúp bạn định nghĩa kiểu dữ liệu cho các biến, tham số và giá trị trả về trong mã nguồn TypeScript, giúp tăng tính chính xác, đồng thời hỗ trợ các công cụ kiểm tra kiểu tĩnh trong quá trình phát triển.

Dưới đây là một số primitives types phổ biến trong TypeScript:

* **number**: Kiểu số, đại diện cho các giá trị số, bao gồm cả số nguyên và số thập phân.
```ts
    const age: number =30;
```

* **string**: Kiểu chuỗi, đại diện cho các giá trị chuỗi ký tự.
```ts
    const name: string = 'TypeScript';
```
* **boolean**: Kiểu logic, đại diện cho hai giá trị là true (đúng) hoặc false (sai).
```ts
    const isStudent: boolean = true;
```
* **null và undefined**: Kiểu dữ liệu null đại diện cho giá trị không tồn tại hoặc không xác định, trong khi kiểu undefined đại diện cho giá trị chưa được gán.
```ts
    let a: null = null;
    let b: undefined = undefined;
```
* **symbol**: Kiểu ký hiệu, đại diện cho một giá trị duy nhất và không thay đổi.
```ts
    const uniqueSymbol: symbol = Symbol("unique");
```
* **bigint**: Kiểu số nguyên lớn, đại diện cho các số nguyên có độ lớn vượt quá phạm vi số nguyên thông thường.
```ts
   const bigNumber: bigint = BigInt(9007199254740991);
```
* **any**: Kiểu dữ liệu mô đun, cho phép biến có bất kỳ kiểu dữ liệu nào và loại kiểu kiểm tra tĩnh.
```ts
    let anyValue: any = "Hello World";
    anyValue = 42;
    anyValue = true;
``` 
* **void**: Kiểu không có giá trị, thường được sử dụng cho các hàm không trả về giá trị.
```ts
    function greet(): void {
    console.log("Hello, world!");
    }
    greet();
``` 

