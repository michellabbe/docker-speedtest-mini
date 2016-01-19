[![Docker Stars](https://img.shields.io/docker/stars/mlabbe/speedtest-mini.svg)](https://hub.docker.com/r/mlabbe/speedtest-mini/) [![Docker Pulls](https://img.shields.io/docker/pulls/mlabbe/speedtest-mini.svg)](https://hub.docker.com/r/mlabbe/speedtest-mini/)

# docker: speedtest-mini

This is a Docker image to run Apache2 and Ookla's [Speedtest Mini](http://www.speedtest.net/fr/mini.php) application for benchmarking network performance.

[![Speedtest Mini](http://www.speedtest.net/images/speedtestmini.png)](http://www.speedtest.net/fr/mini.php)


Total size of this image is:

[![ImageLayers](https://badge.imagelayers.io/mlabbe/speedtest-mini:latest.svg)](https://imagelayers.io/?images=mlabbe/speedtest-mini:latest)

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
docker run --name=speedtest -d -p 80:80 mlabbe/speedtest-mini
```

You can also use a different port if you want.  You can keep the default built-in ports inside the container and just map them to different ports on the host, e.g.:

`-p 8081:80`

At that point, you can use your Docker server as a Speedtest Mini server to begin
benchmarking your network speeds, e.g.:

`http://your_docker_host_ip`
`http://your_docker_host_ip:8081`
