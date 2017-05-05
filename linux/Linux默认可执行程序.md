### Linux默认的可执行文件的位置
* /bin
* /sbin
* /usr/bin
* /usr/sbin

关于Linux默认的文件夹, 请查看```man hier```

### 如何设置可执行文件位置
举个例子:比如我想把```/usr/local/var```作为可执行文件寻找的默认位置, 只需要在.bashrc中添加下面代码即可:
```
export PATH="/usr/local/var:$PATH"
```

*NOTE:我们尽量不要这么做, 因为这样就破坏了linux的文件结构了*

### 如何设置搜索路径的优先级
举个例子:比如在mac系统中使用brew安装php, php会安装在/usr/local/bin, /usr/local/sbin下面. 但是mac系统本身也会有php默认安装文件, 不过他们在/usr/bin, /usr/sbin下面, 我们如何在不改变系统的文件同时, 使用我们安装的php呢? 一个很简单的做法, 改变寻找可执行文件路径的优先级.

`/usr/local/bin`->`/usr/local/sbin`->`/usr/bin`->`/usr/sbin`

修改.bashrc的export为下面的代码:
```
export PATH="/usr/local/bin:/usr/local/sbin:/usr/bin:/bin:/usr/sbin:/sbin"
```

source .bashrc

