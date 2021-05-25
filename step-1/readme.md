Open a shell or terminal and navigate to the repository root (the parent of the folder where this readme is located) and download nwndedicatedserver1.69.zip into it. Then:

    cd step-1/nwserver
    unzip ../../nwndedicatedserver1.69.zip
    tar xzvf linuxdedserver169.tar.gz
    cd ..

Now edit nwnplayer.ini and proceed with

    docker build -t nwserver-step-1 .


Test the image

    docker run -it -p5121:5121/tcp -p5121:5121/udp --rm \
    -v $(pwd)/nwserver/servervault:/opt/nwserver/servervault \
    -v $(pwd)/nwserver/localvault:/opt/nwserver/localvault \
    -v $(pwd)/nwserver/dmvault:/opt/nwserver/dmvault \
    -v $(pwd)/nwserver/saves:/opt/nwserver/saves \
    dockerplay-nws bash -c "./nwserver -interactive"


