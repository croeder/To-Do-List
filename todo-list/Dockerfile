FROM clojure
EXPOSE 3000
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
COPY project.clj /usr/src/app/project.clj
COPY resources /usr/src/app/resources
COPY src /usr/src/app/src
##ADD resources /usr/src/app
##ADD src /usr/src/app
RUN lein deps
RUN echo "RUn.................."
RUN ls /usr/src/app
RUN echo "done RUn.................."

CMD cd  /usr/src/app ; find . -name "*.clj";  lein ring server 
#COPY . /usr/src/app
#RUN mv "$(lein uberjar | sed -n 's/^Created \(.*standalone\.jar\)/\1/p')" app-standalone.jar
#CMD ["java", "-jar", "app-standalone.jar"]

