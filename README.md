# Spring Boot JPA MySQL - Building Rest CRUD API example

For more information about this example visit this web page: https://www.bezkoder.com/spring-boot-angular-17-mysql/

## 1. How to run the Server Spring Boot application
```
mvn spring-boot:run
```

## 2. Install MySQL

https://dev.mysql.com/downloads/installer/

We download the installer file

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/361e37ff-1a76-45c7-bc01-19d874849385)

We execute the installer file

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/7991538f-341f-4386-992e-3964a2a68b40)

We select the **Full** installation

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/5a7c45a2-09ea-4ef7-90f2-6473ac74b658)

We confirm the products to be installed

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/14642e4b-f74e-4831-a254-6cd5b5520ce6)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/6d61cfc7-d23c-4b0d-be06-b91e3f09b0ab)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/4c7af62a-e2c2-42cf-9c2d-99502a092b04)

We configure MySQL during the installation, we leave all the default values:

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/25d24878-6fe1-4f31-a529-a04ddcb7eb6a)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/3b07f023-210b-4849-8204-518d91b0e547)

We set the **password: Luiscoco123456@**

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/9bbcdcb7-8644-4c0e-8260-da4f0d3d9ca2)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/9ca6a26a-aa5e-4906-b993-5567c906fda9)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/9f0e3ef7-8bf5-4c21-80f9-c69748554a4c)

Finally we apply the changes

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/f9b01fa7-44f3-4258-9c72-2fc5ba26d400)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/9a3f593b-7d63-4977-9693-55dd50908a41)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/c32f2d60-171a-49aa-98d1-64ce2831f3c2)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/b0b0c41a-51e0-4c14-8902-7d9a269fcdec)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/f38879b1-233c-40f6-8f01-b8705b9c910e)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/b8cf50ee-101b-471e-9318-cf20c54f5bdc)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/a5413152-6c40-496f-b0b3-5ed5ef5d42e9)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/afa43d26-65bc-45f0-a69b-f7d94aca776a)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/41a46fb6-7c9c-4fd4-96d2-1117d2eb5d3c)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/ff87771b-cb6a-4412-bcf4-9078294f5940)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/583002d8-6620-4f89-bf8c-11c42fb2e6af)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/b8f62bd7-5c95-4e54-9278-c788562bebf8)

## 3. Create the database

We execute MySQL Workbench and we login in the root account

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/b7309da5-07da-42e9-9602-b3e0bac83259)



![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/06a7fe8d-79bf-4638-b1f3-72488dc0a931)

## 3. Source Code explantaion

### 3.1. Dependencies and libraries

The dependencies included in this project are:

- **spring-boot-starter-data-jpa**
- **spring-boot-starter-web**
- **mysql-connector-j**
- **spring-boot-starter-test**

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

### 3.2. Database connection string and other properties 

Regarding the database properties and connections string we set these values in the **application.properties** file:

**application.properties**

```
spring.datasource.url= jdbc:mysql://localhost:3306/testdb?useSSL=false
spring.datasource.username= root
spring.datasource.password= 1234

spring.jpa.properties.hibernate.dialect= org.hibernate.dialect.MySQLDialect
spring.jpa.hibernate.ddl-auto= update
```
