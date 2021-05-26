# NWN Server Docker file - Step 1
FROM i386/debian:buster-slim

# ---------------------------------------------
LABEL Name=NWNCrawl-Base version=1.0

# ---------------------------------------------
WORKDIR /opt/nwserver
COPY ./nwserver /opt/nwserver

# ---------------------------------------------
RUN chown -R root:root * \
    && chmod ug+x fixinstall \
    && ./fixinstall

CMD ["./nwserver", "-interactive"]
