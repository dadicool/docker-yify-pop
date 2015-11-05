docker-yify-pop
===============

Docker build file for yify-pop (Popcorn-time style app with Web UI for YIFY content). You need to have https://www.docker.com/ installed and running to make this useful

*UPDATE* : the YTS api doesn't work anymore (MPAA arggg) so the container works but it can't pull data about movies or shows from anywhere ...

To Run
------

```
docker run -d --name yify-pop -p 4000:4000 -p 8889:8889 dadicool/yify-pop
```

To build
--------

```
git clone https://github.com/dadicool/docker-yify-pop.git
docker build -t yify-pop-custom docker-yify-pop
```

then to run that

```
docker run -d --name yify-pop -p 4000:4000 -p 8889:8889 yify-pop-custom
```

TODO
----
* Run application under non-root user account for better security
* Allow changing port numbers (currently afaict application is expecting fixed numbers)
