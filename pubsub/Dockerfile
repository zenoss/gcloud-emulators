FROM google/cloud-sdk:176.0.0-alpine                                            
RUN apk --update --no-cache add openjdk7-jre
RUN gcloud components install beta pubsub-emulator

ENV CLOUDSDK_CORE_PROJECT=zing-dev

EXPOSE 8085

CMD gcloud beta emulators pubsub start 