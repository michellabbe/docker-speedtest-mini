[![Docker Stars](https://img.shields.io/docker/stars/mlabbe/speedtest-mini.svg)](https://hub.docker.com/r/mlabbe/speedtest-mini/) [![Docker Pulls](https://img.shields.io/docker/pulls/mlabbe/speedtest-mini.svg)](https://hub.docker.com/r/mlabbe/speedtest-mini/)

# docker: speedtest-mini -EXPIRED-
________________________________________
Warning: Speedtest Mini has been discontinued by Oookla.  This image has expired and is no longer usable.

The free Speedtest Custom offered by Ookla as a replacement for Speedtest Mini cannot be run on your own server to test LAN speed (not internet speed).

I have released a new image ([mlabbe/openspeedtest](https://hub.docker.com/r/mlabbe/openspeedtest/)) based on OpenSpeedTest as a replacement image to test LAN speed.
________________________________________


This is a Docker image to run Apache2 and Ookla's [Speedtest Mini](http://www.speedtest.net/fr/mini.php) application for benchmarking network performance.

[![Speedtest Mini](https://raw.githubusercontent.com/michellabbe/docker-speedtest-mini/master/speedtestmini.png)](http://www.speedtest.net/fr/mini.php)

- Runs as non-root user
- Small image size
- Small number of layers

Total size of this image is:

[![](https://images.microbadger.com/badges/image/mlabbe/speedtest-mini.svg)](https://microbadger.com/images/mlabbe/speedtest-mini)

________________________________________
### Pulling from Docker hub
If you want to obtain the image from Docker registry, you can use the following command:
```sh
docker pull mlabbe/speedtest-mini
```
________________________________________
### Running the image
In order to start the speedtest-mini container, use the following:
```sh
docker run --restart=unless-stopped --name=speedtest -d -p 80:8080 mlabbe/speedtest-mini
```

You can also use a different port if you want.  You can keep the default built-in ports inside the container and just map them to different ports on the host, e.g.:

`-p 8081:8080`

At that point, you can use your Docker server as a Speedtest Mini server to begin
benchmarking your network speeds, e.g.:

`http://your_docker_host_ip`
`http://your_docker_host_ip:8081`

________________________________________
### Upgrading
The Speedtest Mini application usually expire after some time so you may need to update the image even though there is no newer build on Docker Hub.

Upgrading the application inside the Docker image is easy.  Just pull the image again from Docker Hub, then stop/remove the container and create it again.  It will download the newer zip file while rebuilding:
```sh
docker pull mlabbe/speedtest-mini
docker stop speedtest
docker rm speedtest
docker run --restart=unless-stopped --name=speedtest -d -p 80:8080 mlabbe/speedtest-mini
```
