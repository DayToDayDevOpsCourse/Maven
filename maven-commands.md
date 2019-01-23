1. Maven lifecycle phases

   validate
   compile
   test
   package
   verify
   install
   deploy
   
2. skip tests execution: -DskipTests=true 

   ex: mvn clean install -DskipTests=true 
   
3. skip tests compilation: -Dmaven.test.skip=true

   ex: mvn clean install -Dmaven.test.skip=true
   
4. Run checkstyle goal on your project: mvn clean install checkstyle:checkstyle

5. Run checkstyle goal on your project & fail the build if any errors/violations: mvn clean install checkstyle:checkstyle checkstyle:check

6. Run checkstyle goal on your project & abd check the error but dont fail the build: mvn clean compile checkstyle:checkstyle checkstyle:check -Dcheckstyle.failOnViolation=false

7. 
