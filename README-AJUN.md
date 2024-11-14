## docker 运行，连接外部mysql 
 Dockerfile-m1
```shell
docker build -t shepher:1.0 -f Dockerfile-m1 .
docker run --name shepher -e MYSQL_HOST=host.docker.internal -e MYSQL_PORT=3307 -p 8085:8089 shepher:1.0
```

## 推送到huawei docker hub
```shell
docker run --name shepher -e MYSQL_HOST=host.docker.internal -e MYSQL_PORT=3307 -p 8085:8089 swr.cn-north-4.myhuaweicloud.com/mewangjun/shepher:1.0

## docker-compose 运行，连接内部mysql
```shell
docker-compose -f docker-compose-m1.yml up
```

