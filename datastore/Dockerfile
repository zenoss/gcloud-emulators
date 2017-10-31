FROM google/cloud-sdk:176.0.0-alpine                                            
RUN apk --update --no-cache add openjdk7-jre
RUN gcloud components install beta cloud-datastore-emulator

ENV DATASTORE_CONSISTENCY=0.9 \
    DATASTORE_DATA_DIR=/var/data \
    CLOUDSDK_CORE_PROJECT=zing-dev

EXPOSE 8081

CMD gcloud beta emulators datastore start \
    --consistency=$DATASTORE_CONSISTENCY \
    --data-dir=$DATASTORE_DATA_DIR