## tutorial page url

https://www.baeldung.com/spring-cloud-data-flow-etl


## manual way
### Downloading Server jars
https://dataflow.spring.io/docs/installation/local/manual/

```shell
wget https://repo.spring.io/release/org/springframework/cloud/spring-cloud-dataflow-server/2.5.3.RELEASE/spring-cloud-dataflow-server-2.5.3.RELEASE.jar
wget https://repo.spring.io/release/org/springframework/cloud/spring-cloud-dataflow-shell/2.5.3.RELEASE/spring-cloud-dataflow-shell-2.5.3.RELEASE.jar
```

### download mysql connector (JDBC driver)
```
https://www.mysql.com/products/connector/
```

### server start
```
$java -Dloader.path=lib -jar spring-cloud-dataflow-server-2.5.3.RELEASE.jar \
--spring.datasource.url=jdbc:mysql://127.0.0.1:3306/dataflow \
--spring.datasource.username=dataflow \
--spring.datasource.password=dataflow \
--spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver \
--spring.rabbitmq.host=127.0.0.1 \
--spring.rabbitmq.port=5672 \
--spring.rabbitmq.username=guest \
--spring.rabbitmq.password=guest
```