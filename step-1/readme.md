Open a shell or terminal and navigate to the repository root (the parent of the folder where this readme is located) and download nwndedicatedserver1.69.zip into it. Then:

    cd step-1/nwserver
    unzip ../../nwndedicatedserver1.69.zip
    tar xzvf linuxdedserver169.tar.gz
    cd ..

Now edit nwnplayer.ini and proceed with

    cp -u nwnplayer.ini nwserver
    docker build -t nwserver-step-1 .


Test the image

    docker run -it -p5121:5121/tcp -p5121:5121/udp --rm \
    -v $(pwd)/nwserver/servervault:/opt/nwserver/servervault \
    -v $(pwd)/nwserver/modules:/opt/nwserver/database \
    -v $(pwd)/nwserver/modules:/opt/nwserver/modules \
    -v $(pwd)/nwserver/saves:/opt/nwserver/saves \
    nwserver-step-1 bash -c "./nwserver -interactive"

You should see:

    Neverwinter Nights Server
    Build:8109
    Copyright BioWare Corp 1998-2004

    Server: Loading...
    Server: Running...

