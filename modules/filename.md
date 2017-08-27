<!-- YAML
added: v0.0.1
-->

<!-- type=var -->

* {string}

当前模块的文件名。也就是对当前模块文件绝对路径的解析。

作为一个主程序，这里的绝对路径没必要和在命令行中使用的一样。

参照当前模块的文件夹名称[`__dirname`][]

示例：

运行位于`/Users/mjr`目录下的`example.js`文件：```node example.js```

```js
console.log(__filename);
// Prints: /Users/mjr/example.js
console.log(__dirname);
// Prints: /Users/mjr
```

给定`a`和`b`两个模块，设定`b`是`a`的一个依赖，以下是两者的目录结构：

* `/Users/mjr/app/a.js`
* `/Users/mjr/app/node_modules/b/b.js`

在`b.js`中引用`__filename`，会返回`/Users/mjr/app/node_modules/b/b.js`
在`a.js`中引用`__filename`，会返回`/Users/mjr/app/a.js`

