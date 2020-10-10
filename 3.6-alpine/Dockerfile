FROM python:3.6-alpine

ARG OPENCV

RUN apk add --no-cache --virtual .build-deps build-base cmake openssl-dev linux-headers \
  && pip install --no-cache-dir scikit-build \
  && pip install --no-cache-dir ${OPENCV} \
  && pip uninstall -y scikit-build \
  && apk del .build-deps
