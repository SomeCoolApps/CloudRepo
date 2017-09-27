FROM openjdk:8 as base
COPY  target/demo-0.0.1-SNAPSHOT.jar /usr/src/myapp/WordServer.jar
WORKDIR /usr/src/myapp
#RUN javac Main.java
#CMD ["java", "Main"]

EXPOSE 8060
 
#install Spring Boot artifact
VOLUME /tmp
RUN sh -c 'touch /usr/src/myapp/WordServer.jar'

#FROM  base as base1:verb
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom  ","-Dspring.profiles.active=verb  ","-jar","/usr/src/myapp/WordServer.jar"]


#FROM  base as base2:noun
#ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom  ","-Dspring.profiles.active=noun  ","-jar","/usr/src/myapp/WordServer.jar"]

#FROM  base as base3:article
#ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom  ","-Dspring.profiles.active=article  ","-jar","/usr/src/myapp/WordServer.jar"]

#FROM  base as base4:adjective
#ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom  ","-Dspring.profiles.active=adjective  ","-jar","/usr/src/myapp/WordServer.jar"]


#FROM  base as base5:subject
#ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom  ","-Dspring.profiles.active=subject  ","-jar","/usr/src/myapp/WordServer.jar"]
