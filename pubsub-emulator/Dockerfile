FROM google/cloud-sdk:alpine

MAINTAINER Noam Y. Tenne <noam@vanmoof.com>

RUN gcloud components install -q pubsub-emulator beta
RUN gcloud components update -q

EXPOSE 8085

CMD ["gcloud", "beta", "emulators", "pubsub", "start", "--host-port", "0.0.0.0:8085"]
