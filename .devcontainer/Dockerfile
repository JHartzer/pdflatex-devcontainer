FROM ubuntu:22.10

# non interactive frontend for locales
ENV DEBIAN_FRONTEND=noninteractive

# installing texlive and utils
RUN apt-get update && \
    apt-get -y install \
        texlive-latex-base \
        texlive-latex-recommended \
        texlive-latex-extra \
        texlive-full \
        git \
        locales && \
    rm -rf /var/lib/apt/lists/*

# Set Locales
RUN sed -i '/en_US.UTF-8/s/^# //g' /etc/locale.gen && locale-gen
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8
