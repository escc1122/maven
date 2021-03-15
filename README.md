# maven

#自訂套件安裝

    mvn install:install-file -Dfile=\local_lib\fastjson-1.2.3.jar -DgroupId=com.alibaba -DartifactId=fastjson -Dversion=1.2.3 -Dpackaging=jar

    <dependency>
        <groupId>com.alibaba</groupId>
        <artifactId>fastjson</artifactId>
    </dependency>
