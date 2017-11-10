FROM google/cloud-sdk:alpine                                            
RUN apk --update --no-cache add openjdk7-jre
RUN gcloud components install beta cloud-datastore-emulator

ENV DATASTORE_CONSISTENCY=0.9 \
    DATASTORE_DATA_DIR=/var/data \
    DATASTORE_HOST_PORT=0.0.0.0:8081 \
    CLOUDSDK_CORE_PROJECT=zing-dev

EXPOSE 8081

CMD gcloud beta emulators datastore start \
    --consistency=$DATASTORE_CONSISTENCY \
    --host-port=$DATASTORE_HOST_PORT \
    --data-dir=$DATASTORE_DATA_DIR
