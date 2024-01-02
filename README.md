# Node.js学习记录

## 本地环境搭建

### 通过官网下载安装包安装
- [Node.js](https://nodejs.org/en)

### 使用包管理工具

#### nvm
- [nvm](https://github.com/nvm-sh/nvm#intro)
- [nvm安装包](https://github.com/coreybutler/nvm-windows/releases)
- nvm命令集合
```
// 设置国内镜像源，可以加快安装速度
nvm node_mirror https://npmmirror.com/mirrors/node/
// 安装指定版本的node
nvm install vx.x.x
// 查看已安装的node版本
nvm ls
// 切换node版本
nvm use vx.x.x
```

#### fnm
- [fnm](https://github.com/Schniz/fnm)
- 使用[chocolatey](https://chocolatey.org/)安装fnm
```
// 安装chcalatey
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
// 安装fnm
choco install fnm
```
- 配置环境变量，推荐使用**git bash**
```
eval "$(fnm env --use-on-cd)
```
![示例](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/cda74cc733794fc586e11a92c8c6d93a~tplv-k3u1fbpfcp-jj-mark:1512:0:0:0:q75.awebp#?w=996&h=448&s=191834&e=gif&f=190&b=000000)
- [fnm命令集合]( fnm:docs/commands.md)
```
// 设置国内镜像源
export FNM_NODE_DIST_MIRROR="https://npmmirror.com/mirrors/node"
// 安装node
// 先将要安装的node版本记录下来
echo 18.16.0 >.node-version
// 执行安装
fnm install
// 查看已安装的版本
fnm list
// 切换node版本
fnm use x.x.x
```


#### volta
- [volta](https://github.com/volta-cli/volta)
- [volta安装包](https://docs.volta.sh/guide/getting-started)
- [volta命令集合](https://docs.volta.sh/reference/)
```
// 安装node
volta install node@x.x.x
// 查看已安装的版本
volta list node
// 切换版本(同安装命令，已存在的版本不会重复安装)
volta install node@x.x.x
```
- 设置项目默认版本,也可以为某个项目设置要使用的版本 (相关配置会自动添加到 package.json 文件中)。
```
volta pin node@x.x.x
```
