FROM java:8
ADD ./system-assemble/target/*.jar /app.jar 
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar","--spring.profiles.active=docker"]
