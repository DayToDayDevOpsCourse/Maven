
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

checkstyle plugin in pom.xml:

            <plugin>
			   <groupId>org.apache.maven.plugins</groupId>
			   <artifactId>maven-checkstyle-plugin</artifactId>
			   <version>3.0.0</version>
			   <executions>
				 <execution>
				   <id>validate</id>
				   <phase>validate</phase>
				   <configuration>
					 <encoding>UTF-8</encoding>
					 <failsOnError>false</failsOnError>
					 <failOnViolation>false</failOnViolation>
				   </configuration>
				   <goals>
					 <goal>check</goal>
					 <goal>checkstyle</goal>
				   </goals>
				 </execution>
			   </executions>
			 </plugin>
