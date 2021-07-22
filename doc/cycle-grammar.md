## for 循环

- **经典 for 循环**

  ```typescript
  for ( init; condition; increment ){
      statement(s);
  }
  
  // 示例
  var i:number =0;
  for (i ; i<10; i++){
      console.log('你好!')
  }
  ```

  它分为三部分组成，init、condition、increment

  **Init 会最先被执行，并且只执行一次**

  然后判断 condition 语句是否为 true，是的话就执行循环，不是就结束循环，每次执行循环前都会判断 condition 语句

  执行完循环体内的代码后就会执行 increment 语句，**这个可以为空，只要保留最后的分号即可**

  

- **for...in 循环**

  for...in 语句用于一组值的集合或列表进行迭代输出。

  ```typescript
  // 列表输出
  var arr:number[] =[2,5,6,7]
  for (var index in arr){
    	// index 索引从0开始
      console.log(arr[index])
  }
  ```

- **for...of 循环**

  for...of 语句创建一个循环来迭代可迭代的对象。在 ES6 中引入的 for...of 循环，以替代 for...in 和 forEach() ，并支持新的迭代协议。for...of 允许你遍历 Arrays（数组）, Strings（字符串）, Maps（映射）, Sets（集合）等可迭代的数据结构等。

  ```typescript
  // 遍历 map
  var map = new Map([
      ['name','greycode'],
      ['desc','打工人']
  ]);
  for (var key of map.keys()){
      console.log(map.get(key))
  }
  
  // 遍历数组
  var arr:number[] =[2,5,6,7]
  for (var value of arr){
      console.log(value)
  }
  
  // 遍历字符串
  var n:string = 'greycode'
  for (var c of n){
      console.log(c)
  }
  ```

- **forEach 循环**

  > 不支持循环体内跳出循环

  ```typescript
  var arr:number[] =[2,5,6,7]
  arr.forEach((val,index,array)=>{
      console.log(val)
      console.log(index)
      console.log(array)
      }
  )
  ```

  上面的三个参数 `val,index,array` 代表着 `值、数组索引值、数组本身`，你可以你可以省略 index 和 array 参数从而单独查询值，比如：

  ```typescript
  var arr:number[] =[2,5,6,7]
  arr.forEach((val)=>{
      console.log(val)
      }
  )
  ```

- **every 循环**

  > 支持循环体内跳出循环，并切必须设置返回布尔值

  ```typescript
   var arr:number[] =[2,5,6,7]
   arr.every((val)=>{
       console.log(val)
     	// 返回 true 时继续执行循环，相当于 continue
     	// 返回 false 时结束循环，相当于 break
     	// 不返回布尔值时结束循环
       return true
       }
   )
  ```

- **some 循环**

  > 支持循环体内跳出循环，但是和 every 不同，布尔返回值时可选的，布尔值的含义和 every 循环相反
  >
  > - 返回 true 相当于 break，会结束循环
  > - 返回 false 相当于 continue，会进入下一次循环

  ```typescript
  var arr:number[] =[2,5,6,7]
  arr.some((val)=>{
      console.log(val)
      }
  )
  ```

## while 循环

基本语法如下：

```typescript
while(flag)
{
   // 当 flag 为 true 时执行
}

```

## do...while 循环

和 while 不同的是它是在尾部判断循环条件，所以会先执行 do 代码块

```typescript
do
{
   // 执行代码块
}while( flag );

// 当 flag 为 true 时会再次执行 do 的代码块
```

## 无限循环

```typescript
// for 无限循环写法
for(;;) { 
   // 语句
}

// while 无限循环写法
while(true) { 
   // 语句
} 

```


