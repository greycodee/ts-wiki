## 类的结构

类用关键字 `class` 来定义一个类，类里面有**字段、构造函数、方法**等信息

```typescript
class LiLei {
    public name:string;

    public constructor(name:string){
        this.name = name;
    }

    public hello(){
        console.log('你好！')
    }
}

// 使用
var lei = new LiLei('李雷')
lei.hello()
```

上面的代码中，变量字段和方法都用了 `public` 修饰符来修饰

在 TypeScript 中，可以用访问控制符来保护对类、变量、方法和构造方法的访问

- **public（默认）** : 公有，可以在任何地方被访问。**在使用中可以省略此字段**
- **protected** : 受保护，可以被其自身以及其子类和父类访问。
- **private** : 私有，只能被其定义所在的类访问。

## 类的继承

用 `extends` 关键字来继承另外一个类，不支持同时继承多个类

```typescript
class Papa {
   
}
class Son extends Papa{
    
}
```



## 静态方法

使用 `static` 关键字来声明类的静态方法或静态变量，静态方法或静态变量可以直接通过类名来访问

```typescript
class Papa {
    static age:number = 30;
    static hello() {
        console.log('this is mama')
    }
}

// 不用实例化 直接访问
Papa.hello()
console.log(Papa.age)
```



## 类和接口

使用 `implements` 来实现接口，支持同时实现多个接口，实现多个接口时，接口直接用 `,` 符号隔开

```typescript
interface IUser{
    name:string;
    sayHi():void;
}

class ZhangSan implements IUser{
    name:string;
    constructor(name:string){
        this.name = name;
    }
    sayHi(){
        console.log("你好，我叫",this.name)
    }
}

// 实例化
var zs = new ZhangSan("张三");
zs.sayHi()
```

实现多个接口

```typescript
interface IUser{
}
interface IAction{
}

class ZhangSan implements IUser,IAction{ 
}
```



## instanceof 运算符

如果要判断一个对象是否是由某个对象实例化而来的可以用 `instanceof` 关键字来判断

```typescript
class ZhangSan{
}
var zs = new ZhangSan()
// 输出 true
console.log(zs instanceof ZhangSan)
```


