# 在线考试反作弊客户端

## 环境准备

1. 安装[Git](https://git-scm.com/)
2. 安装[Node.js](https://nodejs.org/en/)

## 安装Electron和Electron Packager

推荐将Electron和Electron Packager全局化安装，下一次配置时可节省时间

打开Git Bash，输入下面命令：

```
git clone git@github.com:code004Accepted/AntiCheat.git
cd AntiCheat
npm install -g electron
npm install -g electron-packager
```

克隆源码并安装相应的包

您也可以选择一个指定文件夹（比如Desktop）并右键在当前目录打开Git Bash来执行上面的操作，这会使后期编辑代码和链接更加方便

## 测试运行

您可以使用我已经打包好的命令进行测试：

```
npm start
```

看到弹出窗口即为正常，如果不正常，请尝试执行：

```
npm install
npm update
```

## 编辑链接

考虑到每次考试的链接都不相同，您需要在考试前修改`index.html`：

```html
<html>
    <head>
        <meta http-equiv="refresh" content=1;url="https://ks.wjx.top/jq/68052196.aspx
">
    </head>
    <body></body>
</html>

```

将`<meta http-equiv="refresh" content=1;url="https://ks.wjx.top/jq/68052196.aspx
">`中的`https://ks.wjx.top/jq/68052196.aspx`替换为本次考试的链接并保存

## 编译运行

回到Git Bash，运行：

```
npm run packx64
```

为64位系统进行打包

```
npm run ia32
```

为32位系统进行打包

最后，您可以在根目录中的out内看到相应的客户端。

## 尽情享用吧！