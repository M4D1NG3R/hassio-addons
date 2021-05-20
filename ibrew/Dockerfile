FROM python:2.7

RUN apt-get update && apt-get install -y avahi-discover libavahi-compat-libdnssd-dev net-tools git

WORKDIR /opt/app
RUN git clone https://github.com/Tristan79/iBrew.git \
    && pip install -r /opt/app/iBrew/source/requirements.txt \
    && pip install tornado==4.2.1 \
    && pip install -e git+https://github.com/Eichhoernchen/pybonjour.git#egg=pybonjour

EXPOSE 2080

CMD /opt/app/iBrew/source/ibrewui
