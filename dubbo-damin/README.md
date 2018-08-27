## Dubbo-admin
更改zk和密码都通过环境变量改即可

build
```
docker build -t dubbo-admin:latest -f dockerfile .
```
run
```
docker run -d \
-p 8080:8080 \
-e dubbo.registry.address=zookeeper://27.0.0.1:2181 \
-e dubbo.admin.root.password=root \
-e dubbo.admin.guest.password=guest \
dubbo-admin:latest 
```
运行成功后，稍等一下，访问ip:port即可。
默认账号密码是
* 管理员: root:root
* 游客: guest:guest
