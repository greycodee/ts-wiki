## String 

包装类型对象

```typescript
// 声明方式 1
var name:string = 'greycode'
console.log(name)

// 声明方式 2
var name = new String('greycode')
console.log(name.toString())

// 声明方式 3
var name = 'greycode'
console.log(name)
```

此外 String 对象还有许多对象方法，详见：https://www.runoob.com/typescript/ts-string.html

## Number

Number 对象属性和对象方法详解：https://www.runoob.com/typescript/ts-number.html

```typescript
// 声明方式 1
var age:number = 20
console.log(age)

// 声明方式 2
var age = new Number(20)
console.log(age.toString())

// 声明方式 3
var age = 20
console.log(age)
```

## Array 数组

只能存储**同类型的**数据，详解：https://www.runoob.com/typescript/ts-array.html

```typescript
// 声明方式 1
var people:string[] = ['张三','李雷','韩梅梅']

// 声明方式 2
var people = ['张三','李雷','韩梅梅']

// 声明方式 3
var people:string[] = new Array(3)
people[0] = '张三'
people[1] = '李雷'
people[2] = '韩梅梅'

// 声明方式 4
var people:string[] = new Array('张三','李雷','韩梅梅')
```

### 数组解构

下的代码中会按顺序把 **people** 数组里的值分别赋值给 `zz、ll、hmm`

```typescript
var people:string[] = ['张三','李雷','韩梅梅']
var[zs,ll,hmm] = people
console.log(zs)
console.log(ll)
console.log(hmm)
```

## 元组

元组和数组一样，唯一不同的是数组只能存放同一种数据类型，而元组可以存储不同的数据类型

```typescript
// 声明方式
var test = ['张三',10,true]
```

我们可以使用以下两个函数向元组添加新元素或者删除元素：

- push() 向元组添加元素，添加在最后面。
- pop() 从元组中移除元素（最后一个），并返回移除的元素。

元组也和数组一样支持解构

## Map 对象

可以用 `new Map` 来创建一个 Map 对象

```typescript
var map = new Map([
    ['name','greycode'],
    ['age','20']
]);
```

上面代码中，由于没有指定键值对的类型，默认都是 `String` 类型，可以使用下面的代码来为键值对指定类型

```typescript
var map = new Map<string,any>([
    ['name','greycode'],
    ['age',20]
]);
```

Map 相关的函数与属性：

- **map.clear()** – 移除 Map 对象的所有键/值对 。
- **map.set()** – 设置键值对，返回该 Map 对象。
- **map.get()** – 返回键对应的值，如果不存在，则返回 undefined。
- **map.has()** – 返回一个布尔值，用于判断 Map 中是否包含键对应的值。
- **map.delete()** – 删除 Map 中的元素，删除成功返回 true，失败返回 false。
- **map.size** – 返回 Map 对象键/值对的数量。
- **map.keys()** - 返回一个 Iterator 对象， 包含了 Map 对象中每个元素的键 。
- **map.values()** – 返回一个新的Iterator对象，包含了Map对象中每个元素的值 。

## 联合类型

联合类型（Union Types）可以通过管道(|)将变量设置多种类型，赋值时可以根据设置的类型来赋值。

```typescript
// 基本语法格式
var data:type1|type2|type3|...
```

使用：

```typescript
var test:string|number|boolean
test = '这是测试'
test = 9
test = true

// 也可以使用数组
var test:string[]|number[]
test = ['这','是','测','试']
test = [2,4,6,7]

// 或者这样
var test:string[]|string
test = ['这','是','测','试']
test = '这是测试'

// 等等
```


