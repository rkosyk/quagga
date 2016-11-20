# quagga

docker build -t quagga .

docker run -d --restart always -v /opt/docker-quagga:/etc/quagga --name quagga --privileged --network host quagga
