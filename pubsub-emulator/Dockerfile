FROM java:jre-alpine

MAINTAINER Noam Y. Tenne <noam@vanmoof.com>

ENV CLOUDSDK_CORE_DISABLE_PROMPTS 1

RUN apk add --no-cache curl bash python

RUN curl https://sdk.cloud.google.com | bash && \
			/root/google-cloud-sdk/bin/gcloud config set disable_usage_reporting true && \
			/root/google-cloud-sdk/bin/gcloud components install -q pubsub-emulator beta&& \
			/root/google-cloud-sdk/bin/gcloud components update -q 

EXPOSE 8085

CMD ["/root/google-cloud-sdk/bin/gcloud", "beta", "emulators", "pubsub", "start", "--host-port", "0.0.0.0:8085"]
