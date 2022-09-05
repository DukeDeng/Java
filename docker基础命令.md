## 生命周期命令

---

**创建一个容器（不启动它）：**

```
docker create [IMAGE]
```

**重命名现有容器**

```
docker rename [CONTAINER_NAME] [NEW_CONTAINER_NAME]
```

**在新容器中运行命令**

```
docker run [IMAGE] [COMMAND]
```

**退出后移除容器**

```
docker run –rm [IMAGE]
```

**启动一个容器并保持运行**

```
docker run -td [IMAGE]
```

**启动一个容器并在容器中创建一个交互式**

```bash
bash shell docker run -it [IMAGE]
```

**在容器内创建、启动和运行命令，并在执行命令后移除容器。**

```bash
docker run -it-rm [IMAGE]
```

**在已经运行的容器内执行命令。**

```bash
docker exec -it [container]
```

**删除一个容器（如果它没有运行）**

```bash
docker rm [CONTAINER]
```

**更新容器的配置**

```bash
docker update [CONTAINER]
```

---

## 启动和停止容器

**启动容器**

```bash
docker start [CONTAINER]
```

**停止运行容器**

```bash
docker stop [CONTAINER]
```

**停止运行容器并重新启动它**

```bash
docker restart [CONTAINER]
```

**暂停正在运行的容器中的进程**

```bash
docker pause [CONTAINER]
```

**取消暂停正在运行的容器中的进程**

```bash
docker unpause [CONTAINER]
```

**阻塞一个容器直到其他容器停止**

```bash
docker wait [CONTAINER]
```

**通过向正在运行的容器发送**

```bash
SIGKILL
```

**来杀死容器**

```bash
docker kill [CONTAINER]
```

**将本地标准输入、输出和错误流附加到正在运行的容器**

```bash
docker attach [CONTAINER] Docker
```

---

## 镜像命令

**从 Dockerfile 创建镜像**

```bash
docker build [URL/FILE]
```

**从带有标签的 Dockerfile 创建镜像**

```bash
docker build -t [URL/FILE]
```

**从注册表中心拉取镜像**

```bash
docker pull [IMAGE]
```

**将镜像推送到注册中心**

```bash
docker push [IMAGE]
```

**从 tarball 创建镜像**

```bash
docker import [URL/FILE]
```

**从容器创建镜像**

```bash
docker commit [CONTAINER] [NEW_IMAGE_NAME]
```

**删除镜像**

```bash
docker rmi [IMAGE]
```

**从 tar 存档或标准输入加载镜像**

```bash
docker load [TAR_FILE/STDIN_FILE]
```

**将镜像保存到 tar 存档**

```bash
docker save [IMAGE] > [TAR_FILE] Docker
```

**容器和镜像信息 列出正在运行的容器**

```bash
docker ps
```

**列出正在运行的容器和已停止的容器**

```bash
docker ps -a
```

**列出正在运行的容器中的日志**

```bash
docker logs [CONTAINER]
```

**列出 Docker 对象的底层信息**

```bash
docker inspect [OBJECT_NAME/ID]
```

**列出来自容器的实时事件**

```bash
docker events [CONTAINER]
```

**显示容器的端口映射**

```bash
docker port [CONTAINER]
```

**显示容器中正在运行的进程**

```bash
docker top [CONTAINER]
```

**显示容器的实时资源使用统计**

```bash
docker stats [CONTAINER]
```

**显示文件系统上文件（或目录）的更改**

```bash
docker diff [CONTAINER]
```

**列出本地使用 docker 引擎存储的所有镜像**

```bash
docker [image] ls
```

**显示镜像的历史**

```bash
docker history [IMAGE]
```

---

## 网络命令

**列出网络**

```bash
docker network ls
```

**删除一个或多个网络**

```bash
docker network rm [NETWORK]
```

**显示一个或多个网络的信息**

```bash
docker network inspect [NETWORK]
```

**将容器连接到网络**

```bash
docker network connect [NETWORK] [CONTAINER]
```

**断开容器与网络的连接**

```bash
docker network disconnect [NETWORK] [CONTAINER]
```
