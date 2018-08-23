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


