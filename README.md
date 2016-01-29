# springmvc



##1.tomcat 403
add role "manager" to tomcat-users.xml


##2.tomcat 401
add role "manager-gui,manager-scripts" to tomcat-users.xml


##3.settings.xml
```
	<server>settings.xml
		<id>TomcatServer</id>
		<username>tomcat</username>
		<password>tomcat</password>
	</server>
```


##4.pom.xml
```				
<plugin>
	<groupId>org.apache.tomcat.maven</groupId>
	<artifactId>tomcat6-maven-plugin</artifactId>
	<version>2.1</version>
	<configuration>
		<url>http://localhost:8080/manager</url>
		<server>TomcatServer</server>
		<path>/springmvc</path>
	</configuration>
</plugin>
```
