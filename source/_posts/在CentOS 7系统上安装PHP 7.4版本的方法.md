# 在CentOS 7系统上安装PHP 7.4版本的方法

##### 一、添加EPEL和REMI存储库

运行以下命令以添加所需的存储库：

```bash
sudo yum install epel-release
1
sudo yum -y install https://rpms.remirepo.net/enterprise/remi-release-7.rpm
1
```

##### 二、在CentOS 7上安装PHP 7.4版本

我们现在可以启用PHP 7.4 Remi存储库并在CentOS 7上安装PHP 7.4：

```bash
sudo yum -y install yum-utils
1
yum repolist all |grep php
1
sudo yum-config-manager --enable remi-php74
1
```

在CentOS 7上安装PHP 7.4 以及扩展：

```bash
sudo yum install php  php-cli php-fpm php-mysqlnd php-zip php-devel php-gd php-mcrypt php-mbstring php-curl php-xml php-pear php-bcmath php-json php-redis
1
```

当前的PHP版本应为7.4版，如下所示：

```bash
php -v
1
```

如果要查看启用的模块，请运行：

```bash
php --modules
1
```

至此，你已经在CentOS 7上成功安装了PHP 7.4，欢迎使用此版本进行PHP开发/测试。