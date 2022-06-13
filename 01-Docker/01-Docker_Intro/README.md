```
    8  git clone https://github.com/amitvashisttech/docker-kubernetes-ericsson-13-June-2022.git
    9  ls
   10  cd docker-kubernetes-ericsson-13-June-2022/
   11  ls
   12  cp -rf ../old/01-Docker/00-Setup . 
   13  ls
   14  mkdir 01-Docker
   15  mv 00-Setup 01-Docker/
   16  ls
   17  cd 01-Docker/
   18  ls
   19  cd 00-Setup/
   20  s
   21  ls
   22  ./install-docker.sh 
   23  docker version 
   24  ls
   25  cd ..
   26  ls
   27  vim /root/.bashrc 
   28  source /root/.bashrc 
   29  git add . ; git commit -m "01-Docker/00-Setup" ; git push 
   30  history 
   31  git pull 
   32  ls
   33  docker  version 
   34  docker run busybox echo "Welcome to the world of Docker."
   35  docker images 
   36  docker container ls 
   37  docker container ls -a 
   38  docker run busybox echo "Welcome to the world of Docker Test - 1 "
   39  docker images 
   40  docker container ls -a 
   41  docker ps 
   42  docker ps -a 
   43  docker run --name test-2 busybox echo "Welcome to the world of Docker Test - 2"
   44  docker ps -a 
   45  docker run -it  --name test-3 busybox 
   46  docker ps 
   47  docker run -it  --name test-3 busybox 
   48  docker ps 
   49  docker ps -a 
   50  docker start test-3
   51  docker ps 
   52  docker attach test-3
   53  docker ps 
   54  docker kill test-3
   55  docker ps 
   56  docker attach test-3
   57  docker ps 
   58  docker start  test-3
   59  docker ps 
   60  docker inspect test-3
   61  docker run -it  --name test-4 busybox 
   62  docker ps 
   63  docker inspect test-4
   64  docker ps 
   65  docker run -it  --name test-5 busybox 
   66  docker run -itd  --name test-6 busybox 
   67  docker ps 
   68  docker run -itd  --name test-7 busybox 
   69  docker ps 
   70  docker attach test-6
   71  docker ps 
   72  docker ps -a
   73  docker kill test-5
   74  docker ps -a
   75  docker run -d  --name test-8 busybox 
   76  docker ps 
   77  docker ps -a 
   78  docker run -d --name test-nginx-1 nginx 
   79  docker ps 
   80  docker pull ubuntu
   81  docker images 
   82  docker pull ubuntu:16.04
   83  docker images 
   84  cat /etc/os-release 
   85  docker ps 
   86  docker images 
   87  docker run -it -name test-u-1  ubuntu cat /etc/os-release
   88  docker run -it --name test-u-1  ubuntu cat /etc/os-release
   89  docker run -it --name test-u-2  ubuntu:16.04 cat /etc/os-release
   90  docker ps 
   91  docker ps -a 
```
