FROM hhvm/hhvm-proxygen:4.154-latest

ARG WORKSPACE

RUN rm -rf /var/www; ln -s ${WORKSPACE} /var/www
RUN ln -sf /var/www/hhvm.dev.ini /etc/hhvm/site.ini

ADD .deploy/system-init.sh /var/tmp/system-init.sh
RUN touch /.docker_build && /var/tmp/system-init.sh && rm /var/tmp/system-init.sh
