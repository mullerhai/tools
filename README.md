# tools

## These tools  just for virtual cloud compute  machine learning 

### docker  you can  install by  yum  brew  apt-get 

###  deploy.sh  is  for  kubeflow

### ks  is  ksonnet 

### helm   s2i  sti  docker-compose   kubectl  minikube 

### modeldb.jar  is for modeldb package ,you need install  jdk  maven  mongodb  python3  thrift protobuf grpc   nodejs npm sqlite ,then you can run it,some python3 package   lore  grpc-tools  keras  tensorflow  numpy  pandas  sklearn anaconda
### java -jar modeldb-with-dependency.jar

### then you need git clone  modeldb.git  repo  and init  sqlite database use modeldb  generate_database.sh script then you can cd  modeldb frontend  directory ,run  [npm  start] 

### then  you  need  git clone  seldon-core  git repo ,and install seldon-core  on  kubenete,and docker pull some  seldon -wrapper tools

## minikube  kubectl  helm  ks[ksonnet]  s2i  docker-compose sti kubeflow  you need  copy  it to  /usr/local/bin/ or  add  then to the path enviroment variable


### git clone  https://github.com/mitdbg/modeldb.git
### git clone  https://github.com/SeldonIO/seldon-core.git
### git clone thrift 


### docker pull seldonio/seldon-core-s2i-python3:0.1
### docker pull seldonio/core-python-wrapper:0.7

### edit  at 2018-8-23 am 10:31

### some  seldon-core docker images   do not contain some python package  ,you can run it image become container with  /bin/bash,then into the container ,edit python package source change to douban ,https://pypi.douban.com/simple ,and  pip3  install  keras  tensorflow pandas  scipy  grpc-tools. then  docker  commit this container will become new image 


### notice :  some things was wrong  if you want to use helm ,you could choose,one your server  must has global vpn proxy to get googleapi reposity in China ,two  change the  default repo to aliyun and so on 


### maybe you want download some compoment  fast  in China low net speed and  great firewall block ,
###  for docker   suggest use  netease     http://hub-mirror.c.163.com
### for  python pip package  use   htttps://pypi.douban.com/simple
### for helm 
### for kubenete 
### for maven  use  aliyun
### for  scala  sbt use aliyun
### for nodejs  npm use aliyun

### please  use  yum install the virtualbox rpm package  ,because  that can download the dependency by itself
## yum install VirtualBox-5.2-5.2.16_123759_el7-1.x86_64.rpm

## then you do  "minikube start "  it will download  kubenete virtualbox file ,but maybe cannot run ,will has one error !!

#### [root@10 software]# minikube  start
Starting local Kubernetes v1.10.0 cluster...
Starting VM...
E0828 15:22:55.257507   86755 start.go:168] Error starting host: Error creating host: Error executing step: Running precreate checks.
: We support Virtualbox starting with version 5. Your VirtualBox install is "WARNING: The vboxdrv kernel module is not loaded. Either there is no module\n         available for the current kernel (3.10.0-862.9.1.el7.x86_64) or it failed to\n         load. Please recompile the kernel module and install it by\n\n           sudo /sbin/vboxconfig\n\n         You will not be able to start VMs until this problem is fixed.\n5.2.18r124319". Please upgrade at https://www.virtualbox.org.


## then you do  "/usr/lib/virtualbox/vboxdrv.sh setup "  but maybe also has error

##### [root@10 software]# /usr/lib/virtualbox/vboxdrv.sh setup
vboxdrv.sh: Stopping VirtualBox services.
vboxdrv.sh: Starting VirtualBox services.
vboxdrv.sh: Building VirtualBox kernel modules.
This system is currently not set up to build kernel modules.
Please install the Linux kernel "header" files matching the current kernel
for adding new hardware support to the system.
The distribution packages containing the headers are probably:
    kernel-devel kernel-devel-3.10.0-862.9.1.el7.x86_64


### you need  to install   kernel-devel   ,like  the system notice

###  yum install -y kernel-devel-3.10.0-862.9.1.el7.x86_64
### then do " /usr/lib/virtualbox/vboxdrv.sh setup "  again 

### final  do "minikube start "  maybe  it will run normally 

### also  you can  read this  arctile https://blog.csdn.net/liumiaocn/article/details/52041726

## when you  make install  thrift 
thrift 0.11.0
yum install ant -y  [for java compile ]
https://github.com/apache/thrift

http://ftp.wayne.edu/apache/thrift/0.11.0/thrift-0.11.0.tar.gz
https://blog.csdn.net/yangzhenzhen/article/details/77823331

./bootstrap.sh
./configure --enable-coverage --with-go=no --with-golang=no
make  && make install 


### when you want to install grpc 


git clone https://github.com/grpc/grpc.git
cd grpc
git submodule update --init
make
make install
 
 
pip3 install  grpcio-tools


### when you install mongodb
 the config file  like that 
 
 # idae - MongoDB config start - 2016-05-02

# 设置数据文件的存放目录

dbpath = /usr/local/mongodb/bin/data/test/db

# 设置日志文件的存放目录及其日志文件名

logpath = /usr/local/mongodb/bin/data/test/logs/mongodb.log

# 设置端口号（默认的端口号是 27017）

port = 27017

# 设置为以守护进程的方式运行，即在后台运行

#fork = true

# nohttpinterface = true

#nohttpinterface = true

# 配置远程连接

#bind_ip = 0.0.0.0   

#  auth=true 

# idae - MongoDB config end - 2016-05-02


then create db and log directory
mkdir -p  /usr/local/mongodb/bin/data/test/db
mkdir -p    /usr/local/mongodb/bin/data/test/logs/
 



