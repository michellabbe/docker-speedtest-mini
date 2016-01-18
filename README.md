[![Docker Stars](https://img.shields.io/docker/stars/mlabbe/speedtest-mini.svg)](https://hub.docker.com/r/mlabbe/speedtest-mini/) [![Docker Pulls](https://img.shields.io/docker/pulls/mlabbe/speedtest-mini.svg)](https://hub.docker.com/r/mlabbe/speedtest-mini/)

# docker: speedtest-mini

This is a Docker image to run the [Speedtest Mini](http://www.speedtest.net/fr/mini.php) commandline tool for benchmarking network performance.

Total size of this image is:

[![](https://badge.imagelayers.io/mlabbe/speedtest-mini:latest.svg)](https://imagelayers.io/?images=mlabbe/speedtest-mini:latest)

________________________________________
### Pulling from Docker hub
If you want to obtain the image from Docker registry, you can use the following command:
```sh
docker pull mlabbe/speedtest-mini
```
________________________________________
### Running the image
In order to run the speedtest-mini server, use the following:
```sh
docker run --name=speedtest -d -p 80:80 mlabbe/speedtest-mini
```
At that point, you can use your Docker server as a Speedtest Mini server to begin
benchmarking your network speeds.

http://your_docker_host_ip
