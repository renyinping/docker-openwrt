# OpenWrt 14.07 Build System
FROM yinping/openwrt:trusty
MAINTAINER yp_ren@hotmail.com
USER ubuntu

WORKDIR /home/ubuntu
RUN git clone https://git.openwrt.org/14.07/openwrt.git

WORKDIR /home/ubuntu/openwrt
RUN ./scripts/feeds update -a \
 && ./scripts/feeds install -a

WORKDIR /home/ubuntu/openwrt
RUN make download
#RUN make prepare
#RUN make compile
#RUN make clean
#RUN make index

CMD ["sudo","/usr/sbin/sshd","-D"]
