## 类型声明

TypeScript 是一个强类型语言，支持类型声明，比如声明一个 `string` 变量，可以这么写：

```typescript
# 字符串使用单引号
var msg:string = 'hello world'
# 字符串使用双引号
var msg:string = "hello world"
```

字符串可以用单引号括起来，也可以用双引号。

如果你声明了变量的类型，就不可以为这个变量赋予其他类型的值，比如我们把上面的变量赋予 `number` 类型的值

```typescript
var msg:string = 'hello world'
# c
msg = 1
```

此时如果你运行程序，就会报下面的错误

```shell
test.ts:2:1 - error TS2322: Type 'number' is not assignable to type 'string'.
```

## 保留关键字

在声明变量时，不能用以下的保留关键字来声明变量名？

| break    | as         | catch      | switch   |
| -------- | ---------- | ---------- | -------- |
| case     | if         | throw      | else     |
| var      | number     | string     | get      |
| module   | type       | instanceof | typeof   |
| public   | private    | enum       | export   |
| finally  | for        | while      | void     |
| null     | super      | this       | new      |
| in       | return     | true       | false    |
| any      | extends    | static     | let      |
| package  | implements | interface  | function |
| new      | try        | yield      | const    |
| continue | do         |            |          |

## 区分大小写

TypeScript 区分大写和小写字符，比如 `msg` 和大写的 `MSG` 是两个不同的变量

```typescript
var msg:string = 'hello world!'
var MSG:string = '你好 世界!'
console.log(msg)
console.log(MSG)

# 输出
hello world!
你好 世界!
```

## 分号

每行指令都是一段语句，你可以使用分号或不使用， 分号在 TypeScript 中是可选的，建议使用。

以下代码都是合法的：

```typescript
console.log("Runoob")
console.log("Google");
```

如果语句写在同一行则一定需要使用分号来分隔，否则会报错，如：

```typescript
console.log("Runoob");console.log("Google");
```

## 注释

```typescript
// 单行注释

/*
	你好
	这个是
	多行注释
*/
```


