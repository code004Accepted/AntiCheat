# 在线考试反作弊客户端

## 环境准备

1. 安装[Git](https://git-scm.com/)
2. 安装[Node.js](https://nodejs.org/en/)

## 安装Electron和Electron Packager

推荐将Electron和Electron Packager全局化安装，下一次配置时可节省时间

打开Git Bash，依次执行下面步骤：

1. 使用`git clone`克隆本仓库代码；
2. 进入仓库代码目录；
3. 使用`npm`全局安装`electron`和`electron-packager`（选做，因为有人可能已经安装过了，注意如果不是全局安装的建议卸载重装一遍）

参考代码：

```
git clone git@github.com:code004Accepted/AntiCheat.git
cd AntiCheat
```

附注：

1. `npm`安装指令就不需要我多说了吧，自己按自己的需求来；
2. 您也可以选择一个指定文件夹（比如Desktop）并右键在当前目录打开Git Bash来执行上面的操作，这会使后期编辑代码和链接更加方便

## 测试运行

您可以使用下面的命令进行测试：

```
electron .
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

## 打包分发

electron-packager . HelloWorld --platform=win32 --arch=x64 --icon=computer.ico --out=./out --asar --app-version=0.0.1 --overwrite --ignore=node_modules --electron-version 5.0.0

请使用下面格式的命令在Git Bash中打包：

```
electron-packager . <ProjectName> --platform=<Platform> --arch=<Arch> --icon=<PathToIcon> --out=./out --asar --app-version=<AppVersion> --overwrite --electron-version 5.0.0
```

参数注明：
1. <ProjectName>: 生成exe名称
2. <Platform>: 平台：darwin, linux, mas, win32
3. <Arch>: x86, x64
4. <PathToIcon>: ico图标的路径，推荐放置在根目录下，然后就只用写`xxx.ico`了
5. <AppVersion>: 客户端版本

依次为不同系统架构打包后，您就可以在根目录中的out内看到相应的客户端啦~

## 尽情享用吧！

## 附注

1. 需要详细命令，可以查看之前几个Commits的README，里面有更加详细的代码，不过注释说明不太详细qwq

2. 源代码作者code004Accepted(CBJ)，以`GNU General Public License v3.0`授权：

允许：
1. 商业用途
2. 分发
3. 修改
4. 专利授权
5. 私用

要求：
1. 公开源码
2. 放置许可协议与版权信息
3. 使用相同协议
4. 声明变更

禁止：
1. 承担责任

请严格遵守版权协议，否则后果自负