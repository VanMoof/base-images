FROM alpine/gcloud:310.0.0

LABEL mantainer="Juanita De La Cuesta <Juanita@vanmoof.com>"

RUN gcloud components install -q bigtable beta
EXPOSE 8086


RUN echo $BIGTABLE_EMULATOR_HOST
ENTRYPOINT ["gcloud", "beta", "emulators", "bigtable"]
CMD ["start", "--host-port", "0.0.0.0:8086"]

