# Spring Boot JPA MySQL - Building Rest CRUD API example

For more information about this example visit this web page: https://www.bezkoder.com/spring-boot-angular-17-mysql/

## How to run the Server Spring Boot application
```
mvn spring-boot:run
```

## Create MySQL database

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/06a7fe8d-79bf-4638-b1f3-72488dc0a931)

## Source Code explantaion

**pom.xml**

```xml

```


**application.properties**

```
spring.datasource.url= jdbc:mysql://localhost:3306/testdb?useSSL=false
spring.datasource.username= root
spring.datasource.password= 1234

spring.jpa.properties.hibernate.dialect= org.hibernate.dialect.MySQLDialect
spring.jpa.hibernate.ddl-auto= update
```
