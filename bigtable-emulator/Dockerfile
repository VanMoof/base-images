FROM google/cloud-sdk:alpine

MAINTAINER Noam Y. Tenne <noam@vanmoof.com>

RUN gcloud components install -q bigtable beta
RUN gcloud components update -q

EXPOSE 8086

CMD ["gcloud", "beta", "emulators", "bigtable", "start", "--host-port", "0.0.0.0:8086"]
