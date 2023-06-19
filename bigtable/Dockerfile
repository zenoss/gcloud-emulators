FROM google/cloud-sdk:alpine                                            
RUN gcloud components install bigtable beta

ENV CLOUDSDK_CORE_PROJECT=zing-dev \
    HOST_PORT=0.0.0.0:8086

EXPOSE 8086

CMD gcloud beta emulators bigtable start \
    --host-port=$HOST_PORT
