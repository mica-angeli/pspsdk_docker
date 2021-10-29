FROM rangeli93/psp_toolchain:latest

ENV PSPDEV=/usr/local/pspdev
ENV PATH="${PATH}:${PSPDEV}/bin"

WORKDIR /root/
RUN git clone https://github.com/pspdev/pspsdk.git
WORKDIR /root/pspsdk/

RUN ./bootstrap && \
    ./configure && \
    make && \
    make install

