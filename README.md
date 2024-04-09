# Spring Boot JPA MySQL - Building Rest CRUD API example

For more information about this example visit this web page: https://www.bezkoder.com/spring-boot-angular-17-mysql/

## How to run the Server Spring Boot application
```
mvn spring-boot:run
```

## Create MySQL database

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/06a7fe8d-79bf-4638-b1f3-72488dc0a931)

## Source Code explantaion

### Dependencies and libraries

The dependencies included in this project are:

- spring-boot-starter-data-jpa
- spring-boot-starter-web
- mysql-connector-j
- spring-boot-starter-test

This sample is configured for Java 21, hence do not forget to set the JAVA_HOME and/or PATH environmental variable in your local desktop to run this application 

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/14d45f0d-c62e-4718-98fa-91618f770abe)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/80386f51-a518-4256-b9f4-e51affab94b1)

We also can run this command to see the Java version installed in your computer:

```
java --version
```

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/47e181c6-f669-4c4b-af07-d480d428cbae)

We also specify the Java version in the pom.xml file:

```
<properties>
		<java.version>21</java.version>
	</properties>
```

This is the whole pom.xml file:

**pom.xml**

```xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>
	<parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-parent</artifactId>
		<version>3.1.5</version>
		<relativePath />
	</parent>
	<groupId>com.bezkoder</groupId>
	<artifactId>spring-boot-data-jpa</artifactId>
	<version>0.0.1-SNAPSHOT</version>
	<name>spring-boot-data-jpa</name>
	<description>Demo project for Spring Boot Apis CRUD using Spring Data JPA</description>

	<properties>
		<java.version>21</java.version>
	</properties>

	<dependencies>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-jpa</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>

		<dependency>
			<groupId>com.mysql</groupId>
			<artifactId>mysql-connector-j</artifactId>
			<scope>runtime</scope>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
			<exclusions>
				<exclusion>
					<groupId>org.junit.vintage</groupId>
					<artifactId>junit-vintage-engine</artifactId>
				</exclusion>
			</exclusions>
		</dependency>
	</dependencies>

	<build>
		<plugins>
			<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
			</plugin>
		</plugins>
	</build>

</project>
```

Regarding the database properties and connections string we set these values in the **application.properties** file:

**application.properties**

```
spring.datasource.url= jdbc:mysql://localhost:3306/testdb?useSSL=false
spring.datasource.username= root
spring.datasource.password= 1234

spring.jpa.properties.hibernate.dialect= org.hibernate.dialect.MySQLDialect
spring.jpa.hibernate.ddl-auto= update
```
