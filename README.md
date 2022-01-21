# DevOps相关
使用Drone+Gogs+Docker作为解决方案
## 安装
**环境要求**
* Ubuntu 18.04
* Docker
* Docker Compose
* Git

```
# 创建共享网络
docker network create devops
```
### 1. Gogs

```
cd gogs
# 设置docker-compose.yml变量
cp .env.example .env
# 配置
vi .env

# 启动
docker-compose up -d
```
### 2. Drone
Drone 集成两种Runner（Docker Runner和SSH Runner）
```
cd drone
# 设置docker-compose.yml变量
cp .env.example .env
# 配置
vi .env

# 启动
docker-compose up -d
```
