FROM debian:bullseye
COPY config/* /etc/quagga/
RUN apt-get update; \
sudo apt install quagga busybox; #quagga-bgpd может и само поставиться \

sudo /etc/init.d/quagga restart; \
sudo systemctl enable zebra.service; \
sudo systemctl start zebra.service; \
sudo systemctl enable bgpd.service; \
sudo systemctl start bgpd.service; \
