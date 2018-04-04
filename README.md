Parcel 是一个Web应用程序 打包器(bundler) ，与以往的开发人员使用的打包器有所不同。它利用多核处理提供极快的性能，并且你不需要进行任何配置。

首先使用 `Yarn` 或 `npm` 安装 `Parcel` ：

`Yarn`:

>yarn global add parcel-bundler

`npm`:

>npm install -g parcel-bundler

使用以下命令在你的项目目录中创建一个 `package.json` 文件：

>yarn init -y

or

>npm init -y

`Parcel` 可以将任何类型的文件作为 `入口点(entry point)` ，但是 `HTML` 或 `JavaScript` 文件是一个很好的开始。如果你使用相对路径将你的主 `JavaScript` 文件链接到 `HTML` 中，`Parcel` 也会为你处理，并将该引用替换为输出文件的 `URL` 。

接下来，创建一个 `index.html` 和 `index.js` 

```html
<html>
<body>
  <script src="./index.js"></script>
</body>
</html>
```

```javascript
console.log("hello world");
```
Parcel 内置了一个开发服务器，这会在你更改文件时自动重建你的应用程序，并支持 模块热替换 ，以便你快速开发。你只需指定 入口文件 即可：

>parcel index.html

现在在你浏览器中打开 `http://localhost:1234/` 。 您也可以使用 `-p <port number>` 选项覆盖默认端口。