FROM google/cloud-sdk:alpine                                            
RUN apk --update --no-cache add openjdk7-jre
RUN gcloud components install beta pubsub-emulator

ENV CLOUDSDK_CORE_PROJECT=zing-dev \
    PUBSUB_HOST_PORT=0.0.0.0:8085

EXPOSE 8085

CMD gcloud beta emulators pubsub start \
    --host-port=$PUBSUB_HOST_PORT
