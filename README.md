# Create a Spring Boot Application with WAR file

## Utilize SpringBoot Intilizer in Visual Studio Code
1. Download the Spring Initializr Java
ID: 
```
vscjava.vscode-spring-initializr
```
or CTRL+P runn command:
```
ext install vscode-spring-initializr
```
2. Right click on the POM.xml and click on Edit Starters then verify and select dependency and press enter.
3. Open .java source code under src>main>java then click run command above main function.
4. Test your web app by lauching web browser on port 8080 : http://localhost:8080
5. Run Maven to Create a WAR File.

Note: Make sure that Maven and JAVA_HOME are installed and Environment Variables are configured for Maven

6.  Run the following commands under root folder to build, package, test and deploy your container.

```
mvn validate
```
```
mvn compile
```
```
mvn test
```
```
mvn package
```

7.  A temporarely target folder is created with the war file. Since the target file will be deleted, install war file localy or remotely.

    1.  Install war file locally
    ```
    mvn install
    ```
    2.  install war file to a remote repository
    ```
    mvn deploy:deploy-file
    ```
8.  Delete target folder along with war file.
```
mvn clean
```

