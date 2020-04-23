FROM vanmoof/gcloud:latest

MAINTAINER Noam Y. Tenne <noam@vanmoof.com>

RUN bash && /root/google-cloud-sdk/bin/gcloud components install -q pubsub-emulator && \
			/root/google-cloud-sdk/bin/gcloud components update -q 

EXPOSE 8085

CMD ["/root/google-cloud-sdk/bin/gcloud", "beta", "emulators", "pubsub", "start", "--host-port", "0.0.0.0:8085"]
