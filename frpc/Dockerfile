FROM  resin/armv7hf-debian

RUN [ "cross-build-start" ]

RUN apt-get update && apt-get install vim

COPY frpc /usr/local/bin/

RUN chmod +x /usr/local/bin/frpc && \
        mkdir /etc/frp
        
VOLUME /etc/frp

COPY frpc.ini /etc/frp/

CMD ["frpc", "-c", "/etc/frp/frpc.ini"]
RUN [ "cross-build-end" ]

