Step 1: Create a Simple Java Application

Create a file named HelloWorld.java in the src/main/java/com/example directory with the following content:

package com.example;
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, Maven!");
    }
}

Step 2: Create or Modify pom.xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.example</groupId>
    <artifactId>my-java-app</artifactId>
    <version>1.0-SNAPSHOT</version>

    <properties>
        <maven.compiler.source>1.8</maven.compiler.source>
        <maven.compiler.target>1.8</maven.compiler.target>
    </properties>
</project>

Step 3: Build using maven
mvn clean install
This command will compile the Java code, run any tests (if any), and create a JAR file in the target directory.

Step 4: Run the Application
java -cp target/my-java-app-1.0-SNAPSHOT.jar com.example.HelloWorld
This will output:
Hello, Maven!
