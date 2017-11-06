FROM rocker/r-base
LABEL maintainer="Stefan Kuethe <crazycapivara@gmail.com>"
RUN apt-get update && apt-get install -y \
	libcurl4-gnutls-dev \
	libssl-dev \
	libxml2-dev
RUN install2.r miniCRAN
RUN mkdir /miniCRAN
COPY ./scripts /scripts
CMD ["r", "/scripts/create_repo.R"]

