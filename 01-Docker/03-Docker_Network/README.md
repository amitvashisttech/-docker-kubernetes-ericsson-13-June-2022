```
    1  docker ps 
    2  docker run -d --name test-web-server-1 nginx 
    3  docker ps 
    4  docker run -d --name test-1 busybox 
    5  docker ps 
    6  docker ps -a
    7  docker ps 
    8  docker inspect test-web-server-1
    9  docker network ls 
   10  docker network inspect bridge
   11  docker run -d --name test-web-server-2 nginx 
   12  docker network ls 
   13  docker network inspect bridge
   14  ip addr 
   15  docker ps 
   16  curl 172.17.0.2 
   17  curl 172.17.0.3
   18  ip addr 
   19  docker ps 
   20  netstat -tulnp 
   21  docker run -d --name test-web-server-3 -p 8080:80 nginx 
   22  docker ps 
   23  netstat -tulnp 
   24  docker inspect test-web-server-3
   25  systemctl status docker 
   26  docker run -d --name test-web-server-4 -p 8080:80 nginx 
   27  docker run -d --name test-web-server-5 -p 8081:80 nginx 
   28  docker run -d --name test-web-server-6 -p 8082:80 nginx 
   29  docker ps 
   30  docker run -d --name test-web-server-7 -P  nginx 
   31  docker ps 
   32  docker run -d --name my-web -P amitvashist7/mypython-webapp-18-oct-2021:v2
   33  docker ps 
   34  docker run -d --name my-web-1 -P amitvashist7/mypython-webapp-18-oct-2021:v2
   35  docker run -d --name my-web-2 -P amitvashist7/mypython-webapp-18-oct-2021:v2
   36  docker ps 
   37  docker kill $(docker ps -qa ) 
   38  docker rm $(docker ps -qa ) 
   39  ls
   40  cd 01-Docker/
   41  ls
   42  mkdir 03-Docker_Network
   43  ls
   44  cd 03-Docker_Network/
   45  s
   46  history > README.md
```

```
   48  docker network  ls 
   49  docker network create mybr0 --help
   50  docker network create mybr0 -d  "bridge" --subnet=172.28.0.0/16 --ip-range=172.28.5.0/24 --gateway=172.28.5.254 
   51  docker network  ls 
   52  ifconfig 
   53  docker network  inspect mybr0
   54  docker run -d --name my-web-nt-1 -P amitvashist7/mypython-webapp-18-oct-2021:v2
   55  docker run -d --name my-web-nt-2 --network mybr0  -P amitvashist7/mypython-webapp-18-oct-2021:v2
   56  docker run -d --name my-web-nt-3 --network mybr0  -P amitvashist7/mypython-webapp-18-oct-2021:v2
   57  docker ps 
   65  docker inspect --format '{{.Name}} {{.NetworkSettings.Networks.mybr0.IPAddress}}' my-web-nt-3
   66  docker inspect --format '{{.Name}} {{.NetworkSettings.Networks.mybr0.IPAddress}}' my-web-nt-2
   67  docker inspect --format '{{.Name}} {{.NetworkSettings.IPAddress}}' my-web-nt-1
   68  docker ps 
   69  docker network ls 
   70  docker inspect mybr0
   71  docker inspect bridge 
   72  ls
   73  docker network ls 
   74  docker kill $(docker ps -qa) 
   75  docker rm $(docker ps -qa) 
   76  docker network rm mybr0
   77  docker network ls 
```
```
    1  docker run -it --name test-ifconfig ubuntu:16.04 
    2  docker ps 
    3  docker commit -p -m "Net-Tools" test-ifconfig ubuntu-net-tools:16.04 
    4  docker images 
    5  docker run  -itd  --name net-test-1 ubuntu-net-tools:16.04 
    6  docker network ls 
    7  docker run  -itd  --name net-test-2 --network host ubuntu-net-tools:16.04 
    8  docker run  -itd  --name net-test-3 --network none  ubuntu-net-tools:16.04 
    9  docker ps 
   10  docker exec -it net-test-1 ifconfig 
   11  docker network ls 
   12  docker inspect eab1bcf76d83
   13  docker exec -it net-test-3 ifconfig 
   14  docker exec -it net-test-1 ifconfig 
   15  docker exec -it net-test-2 ifconfig 
```
