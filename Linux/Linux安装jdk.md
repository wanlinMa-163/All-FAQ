## 临时

1. 下载镜像。

2. 解压

```sh
# tar -zxvf jdk-8u271-linux-x64.tar.gz
```

3. 设置环境变量

```sh
# # /root/nacosDir/jdk1.8.0_271 是解压后的路径
# export JAVA_HOME=/root/nacosDir/jdk1.8.0_271
# export PATH=$JAVA_HOME/bin:$PATH
# java -version
```

## 永久

#### 推荐配置方式

```sh
vi /etc/profile.d/java.sh
# 添加如下内容
#!/bin/bash
JAVA_HOME=/usr/java/jdk1.8
PATH=$JAVA_HOME/bin:$PATH
export PATH JAVA_HOME

#修改权限
chmod 777 /etc/profile.d/java.sh

# 无效的话执行次命令
# source /etc/profile
```

#### 常见配置方式(不推荐)

```sh
# # /root/nacosDir/jdk1.8.0_271 是解压后的路径
# # 编辑 /etc/profile
# export JAVA_HOME=/root/nacosDir/jdk1.8.0_271/bin
# export PATH=$JAVA_HOME:$PATH
# source /etc/profile
# java -version
```

![image-20201127180607857](images/image-20201127180607857.png)