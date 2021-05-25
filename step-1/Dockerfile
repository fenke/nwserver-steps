# NWN Server Docker file - Step 1
FROM i386/debian:buster-slim

# ---------------------------------------------
LABEL Name=NWNCrawl-Base version=1.0

# ---------------------------------------------
WORKDIR /opt/nwserver
ADD ./nwserver /opt/nwserver

# ---------------------------------------------
RUN chown -R root:root * \
    && chmod ug+x fixinstall \
    && ./fixinstall \
    && apt-get autoremove -y \
    && apt-get clean

CMD ["./nwserver", "-interactive"]
