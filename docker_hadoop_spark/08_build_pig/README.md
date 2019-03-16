﻿**构建 pig 镜像**

## 1.构建镜像
在 [Dockerfile](./Dockerfile) 所在目录下:  
```
docker build -t hs_pig:v1.0 .
```

## 2. 如需获取hadoop-2.7.7安装包    
```
wget -O download/pig-0.17.0.tar.gz http://frp.hnbdata.cn:25081/common/hsdocker/pig-0.17.0.tar.gz
```   
会下载 pig-0.17.0.tar.gz 安装包并存储在 download 文件夹下

