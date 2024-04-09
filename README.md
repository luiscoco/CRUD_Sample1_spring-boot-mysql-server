# Spring Boot JPA MySQL - Building Rest CRUD

For more information about this example visit this web page: https://www.bezkoder.com/spring-boot-angular-17-mysql/

## 1. Install MySQL

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

## 2. Create the database

https://www.w3schools.com/mysql/

We execute MySQL Workbench and we login in the root account.

For the user **root** we remenber the password **Luiscoco123456@** we set during the MySQL installation:

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/b7309da5-07da-42e9-9602-b3e0bac83259)

We run this query for testing the database

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/97e9014c-1423-4212-8731-fd6f26b54ab3)

Now we have to creaete the **testdb** database for this sample 

We first open a new Query tab for this server

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/ceb6813a-e76b-4ab6-9e08-7b5767ac40b0)

We create the database running this query

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/cc80e28f-5590-4915-9ffd-c18f23228c29)

We also have to create the **tutorials** table

```sql
USE testdb
```

```sql
CREATE TABLE tutorials(
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255),
    description TEXT,
    published BOOLEAN,
    createdAt TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP,
    updatedAt TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
);
```

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/d8656a4e-9a33-4f07-be1f-b3848bc59d1b)

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
spring.datasource.password= Luiscoco123456@

spring.jpa.properties.hibernate.dialect= org.hibernate.dialect.MySQLDialect
spring.jpa.hibernate.ddl-auto= update
```

**IMPORTANT NOTE**

Do not forget to set in the application.properties file the MySQL password as defined during installation

```
spring.datasource.password= Luiscoco123456@
```

### 3.3. Project folders and files structure

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/ee1a6f6c-ac8c-4085-a6ee-8f3a8d4a34dd)

### 3.4. Project main entry point

```java
package com.bezkoder.spring.datajpa;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class SpringBootDataJpaApplication {

	public static void main(String[] args) {
		SpringApplication.run(SpringBootDataJpaApplication.class, args);
	}

}
```

### 3.5. Data Model

```java
package com.bezkoder.spring.datajpa.model;

import jakarta.persistence.*;
import java.util.Date;

@Entity
@Table(name = "tutorials")
public class Tutorial {

    @Id
    @GeneratedValue(strategy = GenerationType.AUTO)
    private long id;

    @Column(name = "title")
    private String title;

    @Column(name = "description")
    private String description;

    @Column(name = "published")
    private boolean published;

    @Column(name = "createdAt", nullable = false, updatable = false)
    @Temporal(TemporalType.TIMESTAMP)
    private Date createdAt;

    @Column(name = "updatedAt", nullable = false)
    @Temporal(TemporalType.TIMESTAMP)
    private Date updatedAt;

    public Tutorial() {
    }

    public Tutorial(String title, String description, boolean published) {
        this.title = title;
        this.description = description;
        this.published = published;
    }

    @PrePersist
    protected void onCreate() {
        Date now = new Date();
        this.createdAt = now;
        this.updatedAt = now; // Set updatedAt on create to now
    }

    @PreUpdate
    protected void onUpdate() {
        this.updatedAt = new Date(); // Update updatedAt on every update to now
    }

    // Standard getters and setters

    public long getId() {
        return id;
    }

    public void setId(long id) {
        this.id = id;
    }

    public String getTitle() {
        return title;
    }

    public void setTitle(String title) {
        this.title = title;
    }

    public String getDescription() {
        return description;
    }

    public void setDescription(String description) {
        this.description = description;
    }

    public boolean isPublished() {
        return published;
    }

    public void setPublished(boolean published) {
        this.published = published;
    }

    public Date getCreatedAt() {
        return createdAt;
    }

    // Note: No setter for createdAt to maintain its immutability

    public Date getUpdatedAt() {
        return updatedAt;
    }

    // Note: No direct setter for updatedAt to control its update logic through lifecycle hooks

    @Override
    public String toString() {
        return "Tutorial [id=" + id + ", title=" + title + ", description=" + description + ", published=" + published + ", createdAt=" + createdAt + ", updatedAt=" + updatedAt + "]";
    }
}
```

### 3.6. Jpa Repository

```java #1
package com.bezkoder.spring.datajpa.repository;

import java.util.List;

import org.springframework.data.jpa.repository.JpaRepository;

import com.bezkoder.spring.datajpa.model.Tutorial;

public interface TutorialRepository extends JpaRepository<Tutorial, Long> {
	List<Tutorial> findByPublished(boolean published);
	List<Tutorial> findByTitleContaining(String title);
}
```

### 3.7. Controller

```java
package com.bezkoder.spring.datajpa.controller;

import java.util.ArrayList;
import java.util.List;
import java.util.Optional;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.http.HttpStatus;
import org.springframework.http.ResponseEntity;
import org.springframework.web.bind.annotation.CrossOrigin;
import org.springframework.web.bind.annotation.DeleteMapping;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.PutMapping;
import org.springframework.web.bind.annotation.RequestBody;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;

import com.bezkoder.spring.datajpa.model.Tutorial;
import com.bezkoder.spring.datajpa.repository.TutorialRepository;

@CrossOrigin(origins = "http://localhost:8081")
@RestController
@RequestMapping("/api")
public class TutorialController {

	@Autowired
	TutorialRepository tutorialRepository;

	@GetMapping("/tutorials")
	public ResponseEntity<List<Tutorial>> getAllTutorials(@RequestParam(required = false) String title) {
		try {
			List<Tutorial> tutorials = new ArrayList<Tutorial>();

			if (title == null)
				tutorialRepository.findAll().forEach(tutorials::add);
			else
				tutorialRepository.findByTitleContaining(title).forEach(tutorials::add);

			if (tutorials.isEmpty()) {
				return new ResponseEntity<>(HttpStatus.NO_CONTENT);
			}

			return new ResponseEntity<>(tutorials, HttpStatus.OK);
		} catch (Exception e) {
			return new ResponseEntity<>(null, HttpStatus.INTERNAL_SERVER_ERROR);
		}
	}

	@GetMapping("/tutorials/{id}")
	public ResponseEntity<Tutorial> getTutorialById(@PathVariable("id") long id) {
		Optional<Tutorial> tutorialData = tutorialRepository.findById(id);

		if (tutorialData.isPresent()) {
			return new ResponseEntity<>(tutorialData.get(), HttpStatus.OK);
		} else {
			return new ResponseEntity<>(HttpStatus.NOT_FOUND);
		}
	}

	@PostMapping("/tutorials")
	public ResponseEntity<Tutorial> createTutorial(@RequestBody Tutorial tutorial) {
		try {
			Tutorial _tutorial = tutorialRepository
					.save(new Tutorial(tutorial.getTitle(), tutorial.getDescription(), false));
			return new ResponseEntity<>(_tutorial, HttpStatus.CREATED);
		} catch (Exception e) {
			return new ResponseEntity<>(null, HttpStatus.INTERNAL_SERVER_ERROR);
		}
	}

	@PutMapping("/tutorials/{id}")
	public ResponseEntity<Tutorial> updateTutorial(@PathVariable("id") long id, @RequestBody Tutorial tutorial) {
		Optional<Tutorial> tutorialData = tutorialRepository.findById(id);

		if (tutorialData.isPresent()) {
			Tutorial _tutorial = tutorialData.get();
			_tutorial.setTitle(tutorial.getTitle());
			_tutorial.setDescription(tutorial.getDescription());
			_tutorial.setPublished(tutorial.isPublished());
			return new ResponseEntity<>(tutorialRepository.save(_tutorial), HttpStatus.OK);
		} else {
			return new ResponseEntity<>(HttpStatus.NOT_FOUND);
		}
	}

	@DeleteMapping("/tutorials/{id}")
	public ResponseEntity<HttpStatus> deleteTutorial(@PathVariable("id") long id) {
		try {
			tutorialRepository.deleteById(id);
			return new ResponseEntity<>(HttpStatus.NO_CONTENT);
		} catch (Exception e) {
			return new ResponseEntity<>(HttpStatus.INTERNAL_SERVER_ERROR);
		}
	}

	@DeleteMapping("/tutorials")
	public ResponseEntity<HttpStatus> deleteAllTutorials() {
		try {
			tutorialRepository.deleteAll();
			return new ResponseEntity<>(HttpStatus.NO_CONTENT);
		} catch (Exception e) {
			return new ResponseEntity<>(HttpStatus.INTERNAL_SERVER_ERROR);
		}

	}

	@GetMapping("/tutorials/published")
	public ResponseEntity<List<Tutorial>> findByPublished() {
		try {
			List<Tutorial> tutorials = tutorialRepository.findByPublished(true);

			if (tutorials.isEmpty()) {
				return new ResponseEntity<>(HttpStatus.NO_CONTENT);
			}
			return new ResponseEntity<>(tutorials, HttpStatus.OK);
		} catch (Exception e) {
			return new ResponseEntity<>(HttpStatus.INTERNAL_SERVER_ERROR);
		}
	}

}
```

## 4. How to run the Server SpringBoot application

### 4.1. We first run the Server SpringBoot application

Run MySQL Workbench and enter in the database testdb

```
mvn spring-boot:run
```

or 

```
mvn spring-boot:run -X
```

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/1151909d-7183-4935-bab9-1569d7541beb)

We confirm the SpringBott server application is running in Tomcat in port 8080

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/9f47db9f-ecfe-496e-8cee-db608e75d6db)

### 4.2. We now run the Client Angular front-end application

The Client app source code is stored in this github repo: https://github.com/luiscoco/CRUD_Sample1_angular-17-client

We install the application dependencies with this command:

```
npm i
```

or 

```
npm install
```

Then we run the angular application in port 8081

```
ng serve --port 8081
```

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/d883619d-e13f-4939-a810-8ed2b61ad93d)

We verify the angular application running

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/a2b7ff2d-0e30-402a-b17b-c667169bb77c)

We select the **Add** menu option and we add a new item to the list

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/ed4c7e22-18fc-4ed3-8770-c2cef9800e2f)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/021ee436-ad0c-42e5-81e3-fcd2a559f5e9)

We select the **Tutorials** menu option and we confirm the Tutorial list now has the new created item

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/90cff7ad-cca4-4259-87b4-e29e6573830d)

If we open MySQL Workbench we can also see the new item in the database testdb and table tutorials

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/510ebc64-eb6f-4ce2-8fdf-a504d8dc66ba)

We can also edit the created item pressing on the item and then in the **Edit** button

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/6ac779d9-84b3-4c4e-8950-487e07119f5e)

![image](https://github.com/luiscoco/CRUD_Sample1_spring-boot-mysql-server/assets/32194879/0f6e74e0-a33b-431d-b705-dce19e28d5d6)

