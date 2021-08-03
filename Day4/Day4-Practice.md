# Day4-Practice

## Install Nexus on AWS Linux instance.

   Update the nexus repo username & passowrd details details in maven settings.
   Update the pom.xml with <distributedManagement>
   Update the pom.xml with <repositories> & <pluginRepositories>

## Try with local maven release build.

    Goals: mvn -V clean -B -Dresume=false release:prepare release:perform -Dtag=WebApp-1.0.0-RC-2 -DreleaseVersion=1.0.0-RC-2 -DdevelopmentVersion=1.0.0-SNAPSHOT

## Go to Phase-1.
