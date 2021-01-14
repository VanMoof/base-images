FROM alpine/gcloud:310.0.0

LABEL mantainer="Juanita De La Cuesta <Juanita@vanmoof.com>"

RUN apk add --no-cache openjdk11-jre
RUN gcloud components install -q pubsub-emulator beta

EXPOSE 8085

ENTRYPOINT ["gcloud", "beta", "emulators", "pubsub"]
CMD ["start", "--host-port", "0.0.0.0:8085"]
