# SpringBoot Web + Thymeleaf + Bootstrap

Create a web application with SpringBoot web (MVC), Thymeleaf, Bootstrap.

## Let's start:

Enjoy this!

### Create a new Maven Project

	* Click: File -> New -> MavenProject

	* Check: Create a simple project(skp archtype selection)

	* Click Next

	* Type Group id, Artifact Id and click Finish

### POM Dependencies

Open pom.xml file and add the next code after the </project> tag

```
<dependencies>  	
	<dependency>
	    <groupId>org.springframework.boot</groupId>
	    <artifactId>spring-boot-starter-web</artifactId>
	    <version>2.1.3.RELEASE</version>
	</dependency>
	<dependency>
	    <groupId>org.springframework.boot</groupId>
	    <artifactId>spring-boot-starter-thymeleaf</artifactId>
	    <version>2.1.3.RELEASE</version>
	</dependency>
</dependencies>
```

### Create start class
* create new class file 
* add the annotation @SpringBootApplication before the class
* create a new main method and push this SpringApplication.run(Application.class, args);
* the final code will look like this
```
package springbootthymeleafbootstrap;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class Application {
	public static void main(String[] args) {
		SpringApplication.run(Application.class,args);
	}
}
```

Run main method and see in console application was been started!

...
  o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat started on port(s): 8080 (http) with context path ''
...

### Create a Simple Controller
* create new class file 
* add the annotation @Controller before the class
* create a new method with String return and before the method put @RequestMapping("/") and @ResponseBody annotations
* return any string
* the final code will look like this
```
package springbootthymeleafbootstrap;

import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.RequestMapping;

@Controller
public class IndexController {
	@RequestMapping("/")
	public String index() {
		System.out.println("Controller called");
		return "index";
	}
}
```

### Create template page
 * in src -> main -> resources create a new folder with name templates
 * in template folder create a nem html file (index.html)
 * open html file and paste this code
	```
	<!DOCTYPE html>
	<html>
	<head>
	    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
	    <title>SpringBoot + Thymeleaf - Simple Controller</title>
	    
	</head>
	<body>
	    <div class="container">
	        <div class="jumbotron" align="center" style="margin-top: 50px;">
	            <h1>Welcome!!</h1>            
	        </div>
	    </div>
	    
	</body>
	</html>
	```

Stop application if it's running
Run main method and see in console application was been started!

In the browser open http://localhost:8080/ and see the page.
In the eclipse console see message "Controller called"

### Bootstrap
	* in src -> main -> resources create a new folder with name static
	* [download bootstrap](https://getbootstrap.com/) 
	* Unzip file and rename folder to bootstrap and move to static folder
	* add import tag css before </head> <link href="bootstrap/css/bootstrap.min.css" rel="stylesheet">
	* add import tags jquery, and js before </body> <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script><script src="bootstrap/js/bootstrap.min.js"></script>
	* the final code will look like this
	```
	<!DOCTYPE html>
	<html>
	<head>
	    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
	    <title>SpringBoot + Thymeleaf - Simple Controller</title>
	    <link href="bootstrap/css/bootstrap.min.css" rel="stylesheet">
	</head>
	<body>
	    <div class="container">
	        <div class="jumbotron" align="center" style="margin-top: 50px;">
	            <h1>Welcome!!</h1>            
	        </div>
	    </div>
	    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
	    <script src="bootstrap/js/bootstrap.min.js"></script>
	</body>
	</html>
	```
	
# YWC -> You are Welcome!
