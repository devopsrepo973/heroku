FROM tomcat

RUN apt-get update -y

RUN apt-get install -f

RUN apt-get install git -y

RUN apt-get install nodejs -y

RUN apt-get install npm -y

RUN mkdir -p /tmp/build

WORKDIR /tmp/build/

RUN git clone https://atb@bitbucket.org/atb/tut-basic-gradle-docker.git

WORKDIR /tmp/build/tut-basic-gradle-docker

RUN ./gradlew clean build

RUN cp build/libs/basic-0.0.1-SNAPSHOT.war /usr/local/tomcat/webapps/

EXPOSE 8080
