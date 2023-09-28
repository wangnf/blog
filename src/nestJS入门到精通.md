# nestJS入门到精通

### 初始化项目
```
npm i -g @nestjs/cli

nest new task_back_end
```

### 理解controller
controller 控制器，拦截处理req,res
### 理解service
service服务 主要用于处理公共事件，方法，数据
### module
每个模块都可以抽成一个单独的模块
模块可以导出其中的服务，其他模块可以导入这个这个模块，以方便使用其中的服务

### typeorm
官网：https://typeorm.bootcss.com/example-with-express

方便操作数据库
```
npm install --save @nestjs/typeorm typeorm mysql2
```

### 本地mysql
host: 127.0.0.1
port: 3306
username: root
password: w19921222


-----------------------------------------------------------------------------

### docker启动的mysql服务

1. 启动mysql的容器
```
docker run --name my-mysql -p 32772:3306 -e MYSQL_ROOT_PASSWORD=123456 -d mysql
```

2. 查看所有正在运行的docker容器
```
docker ps
```

3. 查看容器的ip
```
docker inspect -f "{{ .NetworkSettings.Networks.bridge.IPAddress }}" <CONTAINER>
```
将这个 <CONTAINER> 替换为 容器的名称 例如：my-mysql


4. 启动之后，在mac端验证是否能链接
```
nc -vz <REMOTE_SERVER_IP> 32772
```
将这个 <REMOTE_SERVER_IP> 替换为 docker容器的地址 和 ip

5. 





