# Whisky4Steam
install steam in Whisky

# Whisky+Steam 使用教程

### 0x00 前言

参考链接：https://github.com/Whisky-App/Whisky/issues/41

安装之前请保证操作系统的语言设置为英文。

目前配置的Mac系统版本：Sonoma 14.1.2 (23B92)

### 0x01 安装 Whisky

Whisky GitHub 地址：https://github.com/Whisky-App/Whisky

在右侧Release 中找到2.2.1 版本，选择 Whisky.zip 下载。

在访达中，将 Whisky.zip 直接解压，然后将 Whisky 拖入左侧Application，完成添加应用程序的步骤。

### 0x02 下载 Steam 安装包

Steam 官网下载地址：https://store.steampowered.com/about/

选中 Windows 版本下载。

### 0x03 在 Whisky 中创建容器并安装 Steam

打开 Whisky，创建一个容器，名称随意，我设定为 Steam，其他选项默认。等待片刻创建完成后，点击右下角 Run... ，找到 Steam 的安装包进行安装，安装过程中一路点 next，按照默认设置进行安装。安装完成后，不要进行立刻进行 run Steam，取消勾选，然后点击完成。

### 0x04 拷贝 Steam 配置文件

从访达中找到 mac 版 Steam 的路径：`/Users/用户名/Library/Application Support/Steam`

复制三个文件/文件夹：`config`、`registry.vdf`、`userdata`

覆盖到 Whisky 容器中的 Steam 路径：`/Users/用户名/Library/Containers/Whisky/Bottles/你的容器名/drive_c/Program Files (x86)/Steam/`

Tip：即便在0x02的时候自己自定义了容器名称，但在路径中是找不到相应名称的，该名称只是在用户界面展示给用户便于使用，而Whisky 会有自己的一套命名规则来对它命名。如果自己在访达中找不到相关容器路径，可以在 Whisky 中拥有 Steam 的容器中，右下角点击`Open C: Drive`，即可直达该容器的根目录，再依次找寻路径 `/drive_c/Program Files (x86)/Steam/` 即可。

### 0x05 配置 Steam的启动项

等待 Whisky 处理后，会出现 Steam 的图标，右键Steam，选中 Config，在 Argument 一栏中填入启动项 `-allosarches -cef-force-32bit` 

如果没有此步骤，启动 Steam 的时候，将会一直报错 The program steamwebhelper*.*exe has encountered a serious problem and needs to close的崩溃。

### 0x06 启动 Steam

在完成上述所有步骤后，可以双击 Steam 图标或者右键 Steam 选择 Run... 来启动。

至此顺利完成。
