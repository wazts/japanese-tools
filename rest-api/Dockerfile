FROM vertx/vertx3-exec

ENV VERTICLE_NAME com.kaikeru.nihongo.api.Application
ENV VERTICLE_FILE target/rest-api-1.0.0-SNAPSHOT-fat.jar
ENV VERTICLE_HOME /usr/verticles

EXPOSE 8080

COPY $VERTICLE_FILE $VERTICLE_HOME/

WORKDIR $VERTICLE_HOME
ENTRYPOINT ["sh", "-c"]
CMD ["exec vertx run $VERTICLE_NAME -cp $VERTICLE_HOME/*"]
