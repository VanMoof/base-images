FROM google/cloud-sdk:alpine

MAINTAINER Noam Y. Tenne <noam@vanmoof.com>

RUN gcloud components install -q cloud-firestore-emulator beta
RUN gcloud components update -q

EXPOSE 8080

CMD ["gcloud", "beta", "emulators", "firestore", "start", "--host-port", "0.0.0.0:8080"]
