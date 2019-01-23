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

7. mvn dependency:tree

8. mvn versions:set -DnewVersion=2.0.0-SNAPSHOT

9. mvn versions:revert

10. mvn versions:set -DnewVersion=2.0.0-SNAPSHOT -DgenerateBackupPoms=false

11. deploy the file to nexus(Make sure the nexus credentials and repos configured in settings.xml): mvn deploy:deploy-file -Dversion=1.0.0 -DgeneratePom=true -Dpackaging=zip -Dfile=package.zip -DgroupId=com.devops.sample.zip -DartifactId=SampleZip -DrepositoryId=releases -Durl=http://nexus:8081/nexus/content/repositories/releases

12. Download the package from nexus(Make sure the nexus credentials and repos configured in settings.xml): mvn org.apache.maven.plugins:maven-dependency-plugin:3.1.1:get -DrepoUrl=http://nexus:8081/nexus/content/repositories/releases -DgroupId=com.devops.sample.zip -DartifactId=SampleZip -Dversion=1.0.0 -Dpackaging=zip -DrepoId=releases -Ddest=SampleZip.zip
