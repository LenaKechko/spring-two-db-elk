FROM logstash:8.13.0
#FROM logstash:7.16.2

# copy the postgres jdbc driver to the external library folder of logstash
COPY ./bin/ /usr/share/logstash/logstash-core/lib/jars/

COPY config/ /usr/share/logstash/config/

CMD ["logstash", "-f", "/usr/share/logstash/config/usersync.conf"]

RUN /usr/share/logstash/bin/logstash-plugin install --version=3.1.5 logstash-output-mongodb


