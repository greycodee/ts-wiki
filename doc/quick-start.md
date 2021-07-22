## 安装

这里用 npm 工具安装 TypeSctipt

```shell
sudo npm install -g typescript
```

这里的 `-g` 是代表安装到全局环境，如果没有这个的话只会安装到当前执行命令的目录下

执行完命令后，测试下有没有安装成功可以在终端输入 `tsc -v`

```shell
➜  ~ tsc -v
Version 4.3.5
```

看到上面的输出就代表 TypeScript 安装成功了

## 运行一个 ts 文件

浏览器并不能直接运行 TypeScript，需要经过 TypeScript 编译器编译成 JavaScript 后才能运行

![ts-2020-12-01-1](http://cdn.mjava.top/blog/SvOdmwts-2020-12-01-1.png)

在当前目录下新建一个以 `.ts` 结尾的文件

新建 **test.ts** 文件，在文件里输入内容：

```js
var msg:string = 'hello world!'
console.log(msg)
```

然后编译这个 **test.ts** 文件

```shell
tsc test.ts
```

编译完成后，会在当前目录下生成一个同名的 **js 文件**，里面的内容为：

```js
var msg = 'hello world!';
console.log(msg);
```

然后我们用 **nodejs** 来运行这个 js 文件

```shell
node test.js

# 输出
hello world!
```

## 使用 ts-node

如果觉得每次手动编译 ts 文件很麻烦，那么就可以使用 **ts-node** 这个插件了，它会在内部直接帮你编译 ts 文件然后再直接运行，省去手动编译的步骤

安装 ts-node

```shell
sudo npm install -g ts-node
```

运行 ts 文件

```shell
ts-node test.ts

# 输出
hello world!
```

如果你不想安装到全局的话，可以去掉 `-g` 参数，这样的话就只会安装到当前文件夹下

在当前文件夹下会生成一个 **node_modlues** 文件夹，里面有你安装的一些 node 插件模块

这时如果你要编译 ts 文件的话，就要使用 `./node_modules/.bin/ts-node` 这个脚本了

运行 ts 文件

```shell
./node_modules/.bin/ts-node test.ts

# 输出
hello world!
```


