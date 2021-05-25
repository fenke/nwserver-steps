

Test the image

    docker run -it -p5121:5121/tcp -p5121:5121/udp --rm \
    -v $(pwd)/nwserver/servervault:/opt/nwserver/servervault \
    -v $(pwd)/nwserver/localvault:/opt/nwserver/localvault \
    -v $(pwd)/nwserver/dmvault:/opt/nwserver/dmvault \
    -v $(pwd)/nwserver/saves:/opt/nwserver/saves \
    dockerplay-nws bash -c "./nwserver -interactive"


