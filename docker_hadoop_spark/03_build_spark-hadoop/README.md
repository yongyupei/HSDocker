﻿**构建 spark2.1.0 镜像**
>构建spark镜像前先确保构建好前一个hadoop镜像

## 1. 构建镜像
在 [Dockerfile](./Dockerfile) 所在目录下:  
```
docker build --no-cache -t hs_spark-hadoop:v1.0 .
```

## 2. 如需获取hspark2.1.0 安装包    
```
wget -O download/spark-2.2.3-bin-hadoop2.7.tgz https://mirrors.tuna.tsinghua.edu.cn/apache/spark/spark-2.2.3/spark-2.2.3-bin-hadoop2.7.tgz
```   
会下载spark安装包并存储在 download 文件夹下