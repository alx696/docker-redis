# 特点

* 设置时区: **Asia/Shanghai**

## 运行示例

```
$ docker run -d -p 6379:6379 \
  -v ${PWD}/redis:/data \
  --restart=always --name redis xm69/redis \
  redis-server --aof-use-rdb-preamble yes --requirepass mima
```

## 构建

```
$ docker build -t xm69/redis .
```

## 测试

```
$ docker run -it --rm --link 容器名称:lh xm69/redis redis-benchmark -h lh -a 密码 -q -n 100000
```

## 使用cli

```
$ docker run -it --rm --link 容器名称:lh xm69/redis redis-cli -h lh -a 密码
```
