VERSION 0.6

ARG BASE_IMG=debian   # default image
ARG BASE_TAG=bullseye-slim # default tag

# DOCKER_META_VERSION should not be here for cache

FROM ${BASE_IMG}:${BASE_TAG}

docker:
  RUN apt-get update && apt-get install --no-install-recommends -y curl
  ARG DOCKER_META_VERSION
  SAVE IMAGE --push ghcr.io/sksat/debian-curl-docker:${BASE_TAG}-${DOCKER_META_VERSION}
