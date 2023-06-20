FROM google/cloud-sdk:alpine                                         
RUN apk --update --no-cache add openjdk8-jre
RUN gcloud components install beta cloud-firestore-emulator

ENV HOST_PORT=0.0.0.0:8087 \
    CLOUDSDK_CORE_PROJECT=zing-dev

EXPOSE 8087

CMD gcloud beta emulators firestore start \
    --host-port=$HOST_PORT
