FROM google/cloud-sdk:alpine                                        
RUN apk --update --no-cache add openjdk8-jre ca-certificates
RUN gcloud components install beta pubsub-emulator --quiet

ENV CLOUDSDK_CORE_PROJECT=zing-dev \
    HOST_PORT=0.0.0.0:8085

EXPOSE 8085

CMD gcloud beta emulators pubsub start \
    --host-port=$HOST_PORT \
    --verbosity=warning
