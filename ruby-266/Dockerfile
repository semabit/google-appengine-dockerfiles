FROM gcr.io/google_appengine/ruby
# Use the base image provided by Google

# Install ruby and bundler
ARG RUBY_VERSION=2.6.6

RUN cd /rbenv/plugins/ruby-build && \
    git pull && \
    rbenv install -s $RUBY_VERSION && \
    rbenv global $RUBY_VERSION
ENV RBENV_VERSION $RUBY_VERSION

# Install needed libraries
RUN printf "deb http://archive.debian.org/debian/ jessie main\ndeb-src http://archive.debian.org/debian/ jessie main\ndeb http://security.debian.org jessie/updates main\ndeb-src http://security.debian.org jessie/updates main" > /etc/apt/sources.list
RUN apt-get update && apt-get install -y --force-yes -q openssh-client imagemagick
