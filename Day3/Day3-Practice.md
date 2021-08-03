
### To skip the java files from compilation: (through plugin)

    <plugin>
      <groupId>org.apache.maven.plugins</groupId>
      <artifactId>maven-compiler-plugin</artifactId>
      <version>3.1</version>
      <configuration>
        <excludes>
          <exclude>com\devops\calculator\simple\Simple.java</exclude>
        </excludes>
      </configuration>
    </plugin>
    
  ### To skip the test cases compilation & execution (through plugin)
  
      <plugin>
          <groupId>org.apache.maven.plugins</groupId>
          <artifactId>maven-compiler-plugin</artifactId>
          <version>3.1</version>
          <configuration>
            <excludes>
              <exclude>com\devops\calculator\simple\Simple.java</exclude>
            </excludes>
            <skip>true</skip> -->
          </configuration>
        </plugin>
  
##### To skip the test cases execution(using maven command): mvn clean install -DskipTests=true

##### To skip the test cases execution(using maven command): mvn clean install -Dmaven.test.skip=true

##### Run checkstyle goal on your project: mvn clean install checkstyle:checkstyle

##### Run checkstyle goal on your project & fail the build if any errors: mvn clean install checkstyle:checkstyle checkstyle:check

##### Run checkstyle goal on your project & abd check the error but dont fail the build: mvn clean compile checkstyle:checkstyle checkstyle:check -Dcheckstyle.failOnViolation=false
