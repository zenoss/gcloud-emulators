FROM google/cloud-sdk:alpine                                            
RUN apk --update --no-cache add openjdk7-jre
RUN gcloud components install beta bigtable

ENV CLOUDSDK_CORE_PROJECT=zing-dev

EXPOSE 8086

CMD gcloud beta emulators bigtable start