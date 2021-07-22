

## if 语句

这个和 Java 差不多，分为：

- **if 语句** - 只有当指定条件为 true 时，使用该语句来执行代码

  ```typescript
  if ( flag ) {
      // 当 flag 为 true 时执行
  }
  ```

- **if...else 语句** - 当条件为 true 时执行代码，当条件为 false 时执行其他代码

  ```typescript
  if ( flag ){
    // 当 flag 为 true 时执行
  }else {
    // 当 flag 为 false 时执行
  }
  ```

  

- **if...else if....else 语句**- 使用该语句来选择多个代码块之一来执行

  ```typescript
  if ( flag ){
    // 当 flag 为 true 时执行
  }else if ( flag2 ){
    // 当 flag2 为 false 时执行
  }else {
    // 当上面两个条件都为 false 时执行
  }
  ```

## switch 语句

- **switch 语句** - 使用该语句来选择多个代码块之一来执行

  > 不是每一个 case 都需要包含 **break**。如果 case 语句不包含 **break**，控制流将会 *继续* 后续的 case，直到遇到 break 为止。

  ```typescript
  switch(flag){
    case f1:
      // 当 flag=f1 时执行
      break;
    case f2:
      // 当 flag=f2 时执行
     	break;
    default:
      // 当 flag 在上面的 case 中没有匹配项时执行
         }
  ```