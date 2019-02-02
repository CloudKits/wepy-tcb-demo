# TCB in WePY

小程序·云开发是腾讯云提供的后端云能力。

本项目是一个小程序云开发在 WePY 下使用的模板项目，可以帮助开发者快速建立起在 WePY 下的项目，并提供了云函数、云数据库和云存储的调用示例，帮助开发者使用云开发和 WePY 开发小程序。


## 体验步骤

### 1. 安装 wepy
本项目基于wepy开发，[参考这里](https://github.com/wepyjs/wepy)
```bash
yarn global add wepy-cli
```

### 2. 使用本模板初始化项目

使用如下命令来初始化一个名为 `demo` 的小程序

```bash
wepy init cloudkits/wepy-tcb-demo demo
```

### 3. 修改配置项目

由于云开发与小程序绑定，因此，你需要设置一下 `project.config.json`

将其中的 `appid` 的值从 `touristappid` 改为你自己的小程序的 Appid

> 此文件的 Author 等信息根据你的实际项目情况进行修改。

### 4. 开启编译

在 demo 目录下执行如下命令，开启编译

```bash
npm install # 也可以使用 yarn
wepy build --watch
```

### 4. 从小程序开发者工具中导入项目

打开微信小程序开发者工具，点击**新建小程序**，并切换至**导入项目**，将目录选择为你刚刚创建的 Demo 目录，并点击导入。

![](https://ws1.sinaimg.cn/large/006tNc79ly1fzserfw5f7j315u0u0wfr.jpg)

你会看到这样的界面

![](https://ws1.sinaimg.cn/large/006tNc79ly1fzsevb3anbj316m0u0whq.jpg)

### 5. 开通云开发

在开发者工具中点击上方的**云开发**按钮，然后在弹出的界面中初始化云开发。

初始化完成后，你需要点击上方的 **数据库**，前往创建一个测试集合,添加一个名为 `test` 的集合。

![](https://ws3.sinaimg.cn/large/006tNc79ly1fzsewpormcj30v20a0aa3.jpg)

创建完成后，关闭云开发控制台。


### 6. 部署云函数

在编辑器中，找到 `cloudfunctions/getOpenID`，并在其上面右击，选择**创建并部署：云端安装依赖**（或上传并部署：云端安装依赖），部署云函数。

![](https://ws3.sinaimg.cn/large/006tNc79ly1fzsexv1jk5j30vm0pwtae.jpg)

### 7. 试用云开发

当你配置完成后，可以点击预览界面的三个按钮，依次测试云开发的云函数、云数据库、文件存储的功能。

效果图如下：

![](https://ws2.sinaimg.cn/large/006tNc79ly1fzsezp573qj30js0xogm5.jpg)
