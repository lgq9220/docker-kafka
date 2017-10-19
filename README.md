# docker-kafka
快速部署Kafka，适用于本地开发测试环境

# Usage
- 启动 Kafka:
```
docker-compose up -d
```
- 关闭 Kafka:
```
docker-compose stop
```
- 运行 Kafka 命令：（以显示 topics 列表为例，其它命令请参考：[Kafka Quickstart](http://kafka.apache.org/quickstart)）
```
docker exec -it {容器Id} kafka-topics.sh --list --zookeeper localhost:2181

说明：这里的 zookeeper 地址写法固定为 localhost:2181，因为这个Docker内部自启动了 zookeeper 不需要外部环境支持
```
