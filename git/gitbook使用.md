### 安装node
方法1: 打开 https://nodejs.org/ 点击绿色的 INSTALL 按钮下载安装 node，npm会随着安装包一起安装
方法2: mac下brew install gitbook

### 安装gitbook
npm install gitbook-cli -g

### 初始化项目
gitbook init

在目录下会新创建两个文件**README.md**和**SUMMARY.md**

对SUMMARY.md进行编辑, 然后执行gitbook init, gitbook init 会根据 SUMMARY.md 目录生成对应的文件夹和 md 文件

### gitbook build

gitbook build <output path>

### git server
使用gitbook server启动gitbook服务