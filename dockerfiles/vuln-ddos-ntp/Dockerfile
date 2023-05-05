FROM ubuntu:14.04

RUN apt update && apt install --yes ntp
COPY ./ntp.conf /etc/ntp.conf
EXPOSE 123/udp
#ENTRYPOINT ["/usr/sbin/ntpd", "--nofork"]
CMD /usr/sbin/ntpd -c /etc/ntp.conf -n -l stdout
