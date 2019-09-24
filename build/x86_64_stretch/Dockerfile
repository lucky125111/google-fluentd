FROM debian:9.9

RUN apt-get update -y \
 && apt-get install -y \
        autoconf \
        bzip2 \
        cmake \
        curl \
        fakeroot \
        git \
        gnupg \
        g++ \
        libicu-dev \
        make \
        procps \
  && gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB \
  && git config --global user.email "stackdriver-github-reader@google.com" \
  && git config --global user.name "stackdriverreader" \
  && (curl -sSL https://get.rvm.io | /bin/bash -s stable) \
  && /bin/bash -l -c "rvm requirements && rvm install 2.4 && gem install bundler --no-document && gem update"
