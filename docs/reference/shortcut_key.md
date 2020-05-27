# MAC 常用工具快捷键与命令行操作

## VI

### 查找替换
1. 

### 光标移动
1.  行首
2.  行尾


## SHELL
### 光标移动
1. control+a 行首
2. control+e 行尾

## Docker
### 查看镜像
```
docker images
```
### 删除镜像 
```
docker rmi [image/ID]
docker image rm [image/ID]
支持的子命令
-f, -force: 强制删除镜像，即便有容器引用该镜像
-no-prune: 不要删除未带标签的父镜像
```
### 清理镜像
```
docker image prune
支持的子命令
-a, --all: 删除所有没有用的镜像，而不仅仅是临时文件
-f, --force: 强制删除镜像文件，无需弹出提示确认
```