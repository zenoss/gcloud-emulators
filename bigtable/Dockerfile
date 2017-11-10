FROM google/cloud-sdk:alpine                                            
RUN apk --update --no-cache add openjdk7-jre
RUN gcloud components install beta bigtable

ENV CLOUDSDK_CORE_PROJECT=zing-dev \
    BIGTABLE_HOST_PORT=0.0.0.0:8086

EXPOSE 8086

CMD gcloud beta emulators bigtable start \
    --host-port=$BIGTABLE_HOST_PORT
