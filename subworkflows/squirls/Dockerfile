FROM ubuntu:22.04

# Configuring TZ to avoid halting git installation
ENV TZ=Europe/London
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# Installing necessary utilities and dependencies
RUN  apt-get update \
	&& apt-get upgrade -y \
	&& apt-get install -y default-jdk \
	&& apt-get install -y unzip \
	&& apt-get install -y wget

# Download SQUIRLS v2.0.0 release
RUN wget https://github.com/TheJacksonLaboratory/Squirls/releases/download/v2.0.0/squirls-cli-2.0.0-distribution.zip \
	&& unzip squirls-cli-2.0.0-distribution.zip