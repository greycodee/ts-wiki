## 接口

和 Java 一样，TypeScript 的接口也是用关键字 `interface` 来声明的

```typescript
interface IUser{

}
```

使用：

```typescript
interface IUser{
    name:string
    age:number
    sayHi():void
}

var zhansan:IUser = {
    name: '张三',
    age: 20,
    sayHi(){
        console.log('我是',this.name,'，今年',this.age,'岁')
    }
}

zhansan.sayHi()
```

## 接口继承

接口可以使用 `extends` 关键字继承其他接口。

```typescript
interface IAction {
    run():void
}
interface IUser extends IAction {
    name:string
    age:number
    sayHi():void
}
var zhansan:IUser = {
    name: '张三',
    age: 20,
    sayHi(){
        console.log('我是',this.name,'，今年',this.age,'岁')
    },
    run(){
        console.log('我会跑')
    }
}
```


