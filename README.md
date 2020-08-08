## tutorial page url

https://www.baeldung.com/spring-cloud-data-flow-etl

https://github.com/eugenp/tutorials/tree/master/spring-cloud-data-flow/spring-cloud-data-flow-etl

## reference

https://dataflow.spring.io/docs/concepts/architecture/

## manual way
### Downloading Server jars
https://dataflow.spring.io/docs/installation/local/manual/

```shell
wget https://repo.spring.io/release/org/springframework/cloud/spring-cloud-dataflow-server/2.5.3.RELEASE/spring-cloud-dataflow-server-2.5.3.RELEASE.jar
wget https://repo.spring.io/release/org/springframework/cloud/spring-cloud-dataflow-shell/2.5.3.RELEASE/spring-cloud-dataflow-shell-2.5.3.RELEASE.jar
wget wget https://repo.spring.io/release/org/springframework/cloud/spring-cloud-skipper-server/2.5.0/spring-cloud-skipper-server-2.5.0.jar
```

### download mysql connector (JDBC driver)
```
https://www.mysql.com/products/connector/
```

### skipper start
```
$ java -jar spring-cloud-skipper-server-2.5.0.jar
```

### server start
```
$ java -jar spring-cloud-dataflow-server-2.5.3.RELEASE.jar \
--spring.datasource.url=jdbc:mysql://127.0.0.1:3306/dataflow \
--spring.datasource.username=dataflow \
--spring.datasource.password=dataflow \
--spring.datasource.driver-class-name=org.mariadb.jdbc.Driver \
--spring.rabbitmq.host=127.0.0.1 \
--spring.rabbitmq.port=5672 \
--spring.rabbitmq.username=guest \
--spring.rabbitmq.password=guest
```


### shell

## run shell
```
java -jar spring-cloud-dataflow-shell-2.5.3.RELEASE.jar
```

### connect server in shell
```shell
server-unknown:>dataflow config server http://localhost:9393
```
