镜像参考 copy docker pull eugeneware/docker-wordpress-nginx

简单使用

```bash
$ git clone https://github.com/ivaners/docker-lnmp.git
$ cd docker-lnmp
$ sudo docker build -t="docker-lnmp" .
```

## Usage

To spawn a new instance of wordpress on port 80.  The -p 80:80 maps the internal docker port 80 to the outside port 80 of the host machine.

```bash
$ sudo docker run -p 80:80 -v /home/ivan/www:/usr/share/nginx/www --name docker-lnmp -d docker-lnmp
```

Start your newly created docker.

```
$ sudo docker start docker-lnmp
```

After starting the docker-wordpress-nginx check to see if it started and the port mapping is correct.  This will also report the port mapping between the docker container and the host machine.

```
$ sudo docker ps

0.0.0.0:80 -> 80/tcp docker-lnmp
```

You can the visit the following URL in a browser on your host machine to get started:

```
http://127.0.0.1:80
```
