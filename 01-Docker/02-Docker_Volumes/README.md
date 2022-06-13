```
    1  docker volume ls 
    2  docker volume create my-vol
    3  docker volume ls 
    4  docker volume inspect my-vol
    5  ls -ltr /var/lib/docker/volumes/my-vol/_data
    6  cd 
    7  docker run -it --name vol-test-1 -v my-vol:/var/www/html/amitv ubuntu:16.04 
    8  docker ps -a 
    9  docker rm vol-test-1
   10  docker ps -a 
   11  docker volume ls 
   12  cat /var/lib/docker/volumes/my-vol/_data/myvol-test-example/hello.txt 
```

```
   24  docker run -it --name vol-test-2 -v /var/www/html/myapp ubuntu:16.04 
   25  docker ps 
   26  docker inspect $(docker ps -ql) 
   27  ls
   28  docker volume ls 
   29  ls -ltr /var/lib/docker/volumes/6a06774a6c21436efb6bfdae7b5dce25fc8ae828b4949945941fb6980792b453/_data/abc.txt 
   30  cat  /var/lib/docker/volumes/6a06774a6c21436efb6bfdae7b5dce25fc8ae828b4949945941fb6980792b453/_data/abc.txt 
   31  docker ps 
   32  cat  /var/lib/docker/volumes/6a06774a6c21436efb6bfdae7b5dce25fc8ae828b4949945941fb6980792b453/_data/abc.txt 
   33  hostname -f >> /var/lib/docker/volumes/6a06774a6c21436efb6bfdae7b5dce25fc8ae828b4949945941fb6980792b453/_data/abc.txt
   34  date >> /var/lib/docker/volumes/6a06774a6c21436efb6bfdae7b5dce25fc8ae828b4949945941fb6980792b453/_data/abc.txt
   35  cat  /var/lib/docker/volumes/6a06774a6c21436efb6bfdae7b5dce25fc8ae828b4949945941fb6980792b453/_data/abc.txt 
   36  docker ps -l
   37  docker attach  $(docker ps -ql) 
   38  docker kill   $(docker ps -ql) 
   39  docker rm   $(docker ps -ql) 
   40  docker ps -qa 
   41  docker volume ls 
   42  docker volume -q
   43  docker volume ls -q
   44  docker volume rm $(docker volume ls -q) 
   45  docker volume ls -q
```

```
    1 ls -ltr /var/lib/docker/volumes/
    2  ls
    3  docker run --name vol-test-3 -v /root/docker-kubernetes-ericsson-13-June-2022:/myapp ubuntu:16.04 
    4  docker run -it --name vol-test-4 -v /root/docker-kubernetes-ericsson-13-June-2022:/myapp ubuntu:16.04 
    5  docker ps 
    6  docker inspect vol-test-4
    7  docker run -it --name vol-test-5 -v /root/docker-kubernetes-ericsson-13-June-2022:/myapp:ro ubuntu:16.04 
    8  docker ps 
    9  docker inspect vol-test-5
   10  ls
   11  history >> docker-kubernetes-ericsson-13-June-2022/01-Docker/02-Docker_Volumes/README.md 
```  
  
```
    1  docker run -itd --name data-vol -v /var/www/html/amit -v /etc/amit -v /var/log/amit ubuntu:16.04 
    2  docker ps 
    3  docker inspect data-vol
    4  docker run -itd --name data-vol-test-1 --volume-from data-vol ubuntu:16.04 
    5  docker run -itd --name data-vol-test-1 --volumes-from data-vol ubuntu:16.04 
    6  docker run -itd --name data-vol-test-2 --volumes-from data-vol ubuntu:16.04 
    7  docker run -itd --name data-vol-test-3 --volumes-from data-vol ubuntu:16.04 
    8  docker ps 
    9  docker inspect data-vol-test-1
   10  docker inspect data-vol-test-2
   11  docker attach data-vol-test-2
   12  docker ps 
   13  docker exec -it data-vol-test-1 cat /etc/amit/hello
   14  docker exec -it data-vol-test-2 cat /etc/amit/hello
   15  docker exec -it data-vol-test-3 cat /etc/amit/hello
   16  docker exec -it data-vol cat /etc/amit/hello
   17  docker exec -it vol-test-5 cat /etc/amit/hello
   18  docker volume ls 
   19  cat /var/lib/docker/volumes/b952a717562d636797bc1ecc6aeede402776ccd05dd17c366887952045386d42/_data/
   20  cat /var/lib/docker/volumes/edd9a9e93d333a64efc0a7e9bbf51428b5c6914d4d54c9175b1f239e56f95e72/_data/
   21  cat /var/lib/docker/volumes/f000dbf2e10c393bb0e62a729ddc090fe689c499c118e34829bb98b907ec7e7c/_data/hello 
   22  history >> docker-kubernetes-ericsson-13-June-2022/01-Docker/02-Docker_Volumes/README.md 
```
