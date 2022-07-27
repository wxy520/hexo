# 编译安装 php 7.4 no package ‘oniguruma’ found

### 错误日志

```bash
No package 'oniguruma' found

Consider adjusting the PKG_CONFIG_PATH environment variable if you
installed software in a non-standard prefix.

Alternatively, you may set the environment variables ONIG_CFLAGS
and ONIG_LIBS to avoid the need to call pkg-config.
See the pkg-config man page for more details.
```



### 解决方法

安装 `oniguruma` 和 `oniguruma-devel` 软件包

这两个人软件包没有被添加进大多数软件源中，可以点击 https://pkgs.org/download/oniguruma 和 https://pkgs.org/download/oniguruma-devel 下载

### Ubuntu

直接执行以下命令安装

```bash
sudo apt install libonig-dev
```



### Centos 7

直接执行以下命令即可安装

```bash
yum install https://rpms.remirepo.net/enterprise/7/remi/x86_64/oniguruma5php-6.9.6-1.el7.remi.x86_64.rpm
yum install https://rpms.remirepo.net/enterprise/7/remi/x86_64/oniguruma5php-devel-6.9.6-1.el7.remi.x86_64.rpm
```



### 软件包链接失效问题

链接随时有可能因软件包包版本更新而失效，读者可以通过这里的链接搜索 [oniguruma5php](https://pkgs.org/download/oniguruma5php) 和 [oniguruma5php-devel](https://pkgs.org/download/oniguruma5php-devel) 软件包 （只对 Centos 有效，其他发行版请使用 解决方法 中的链接）

将对应链接替换为相应 Binary Package，并在讨论区留言方便其他读者解决此问题