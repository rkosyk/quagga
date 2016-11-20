# quagga


1) Configure quagga in the docker-quagga folder

2) Build an image

docker build -t quagga .

3) Run the container in the "privileged" mode and network type "host"

docker run -d --restart always -v quagga:/etc/quagga --name quagga --privileged --network host quagga

== OR ===============================================================================================

1) Build an image

docker build -t quagga .

2) Run the container in the "privileged" mode and network type "host" and host attached folder "/opt/docker-quagga"

docker run -d --restart always -v /opt/docker-quagga:/etc/quagga --name quagga --privileged --network host quagga

3) Configure quagga in "/opt/docker-quagga"

4) Restart the quagga container

docker restart quagga
