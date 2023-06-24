FROM fluent/fluentd:v1.14.2-debian-1.0

USER root
WORKDIR /home/fluent

# Install Fluentd plugins
RUN gem install fluent-plugin-elasticsearch -v 5.0.3 \
    && gem install fluent-plugin-json 

# Copy Fluentd configuration file
COPY fluent.conf /fluentd/etc/fluent.conf

CMD ["fluentd", "-c", "/fluentd/etc/fluent.conf"]
