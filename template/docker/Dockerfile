FROM debian:12
RUN apt-get update && apt-get dist-upgrade -y

RUN apt-get update && apt-get install -y --no-install-recommends \
    make \
    gzip \
    tar \
    wget ca-certificates openssl \
    zip

# debian 12 has KiCad 6.0 by default - installing 7.0 from newer rc instead
#RUN apt-get update && apt-get install -y --no-install-recommends \
#    kicad \
#    kicad-packages3d
RUN cd /tmp/ && \
    wget "https://ftp.debian.org/debian/pool/main/k/kicad/kicad_7.0.8+dfsg-1~bpo12+1_amd64.deb" && \
    wget "https://ftp.debian.org/debian/pool/main/k/kicad/kicad-libraries_7.0.8+dfsg-1_all.deb" && \
    wget "https://ftp.debian.org/debian/pool/main/k/kicad-footprints/kicad-footprints_7.0.8-1~bpo12+1_all.deb" && \
    wget "https://ftp.debian.org/debian/pool/main/k/kicad-packages3d/kicad-packages3d_7.0.8-1~bpo12+1_all.deb" && \
    wget "https://ftp.debian.org/debian/pool/main/k/kicad-symbols/kicad-symbols_7.0.8-1~bpo12+1_all.deb" && \
    wget "https://ftp.debian.org/debian/pool/main/k/kicad-templates/kicad-templates_7.0.8-1~bpo12+1_all.deb" && \
    apt-get install -y ./*.deb && \
    rm *.deb

RUN apt-get update && apt-get install -y --no-install-recommends \
    prusa-slicer

COPY \
  generate_bom \
  generate_gerber \
  generate_stl \
  /usr/local/bin/

ENV HOME=/tmp/
RUN mkdir -p "/tmp/.config/"
COPY kicad /tmp/.config/kicad
RUN chmod a+rw -R "/tmp/.config/"
