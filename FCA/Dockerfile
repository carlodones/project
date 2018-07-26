FROM resin/raspberry-pi3-debian:jessie

RUN apt-get update && apt-get install -yq \
   python3 python sense-hat raspberrypi-bootloader python-pip python3-pip && \
   pip install MinimalModbus && \
   pip install modbus_tk && \
   pip install paho-mqtt && \
   apt-get clean && rm -rf /var/lib/apt/lists/*

WORKDIR /usr/src/FCA

COPY . .

ENV INITSYSTEM on

#CMD ["python", "/usr/src/src/thread_sense.py"]

CMD ["python", "usr/src/FCA/src/MODBUS/tMODUBUS.py"]


