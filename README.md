# maven

#自訂套件安裝

    mvn install:install-file -Dfile=\local_lib\fastjson-1.2.3.jar -DgroupId=com.alibaba -DartifactId=fastjson -Dversion=1.2.3 -Dpackaging=jar

    <dependency>
        <groupId>com.alibaba</groupId>
        <artifactId>fastjson</artifactId>
        <version>1.2.3</version>
    </dependency>
    
    
    
    
    
    
    
# Nexus

參考
https://hub.docker.com/r/sonatype/nexus3

https://kknews.cc/zh-tw/education/pgoqap2.html


安裝

docker run -d -p 8083:8081 --name nexus sonatype/nexus3

mvn settings

	<server>
		<id>al_test</id>
		<username>admin</username>
		<password>11111111</password>
	</server>


pom.xml

    <repositories>
        <repository>
            <id>al_test</id>
            <name>Team Nexus Repository</name>
            <url>http://127.0.0.1:8081/repository/al_test/</url>
        </repository>
    </repositories>



deploy
mvn deploy:deploy-file -DgroupId=cn.kbyte.utils -DartifactId=phone-number-geo -Dversion=0.1 -Dpackaging=jar -Dfile=D:\phone-number-geo\target\phone-number-geo-0.1.jar -Durl=http://127.0.0.1:8081/repository/al_test/ -DrepositoryId=al_test


# source root
https://confluence.jetbrains.com/display/IDEADEV/Maven+Integration+FAQ

	<build>
	 <sourceDirectory>...</sourceDirectory> will be added as Source folder
	 <testSourceDirectory>...</testSourceDirectory> will be added as Test Source folder

	 <resources>
	  <resource>
	   <directory>...</directory> will be added as Source folder
	  </resource>
	 <resources>

	 <testResources>
	  <testResource>
	   <directory>...</directory> will be added as Test Source folder
	  </testResource>
	 /<testResources>
	</build>



# 參考

maven 標準目錄

https://maven.apache.org/guides/introduction/introduction-to-the-standard-directory-layout.html

