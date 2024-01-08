# NWN Server Docker file - Step 1
FROM beamdog/nwserver:latest

# ---------------------------------------------
LABEL Name=NWNCrawl-Beamdog version=1.0
ENV NWN_PUBLICSERVER 0
ENV NWN_SERVERNAME NWNDungeonCrawl

# ---------------------------------------------
WORKDIR /nwn/data/bin/linux-x86
# ---------------------------------------------
CMD ["/nwn/run-server.sh", "publicserver 0"]
