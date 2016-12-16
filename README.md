# superset_deploy
Deploy for superset

#step 1:get resource

git clone https://github.com/tddv/superset_deploy.git

#step 2:install docker-compose  and docker

sudo apt-get update

sudo apt-get install docker.io

sudo apt-get install python-pip

sudo pip uninstall docker-compose

sudo pip install docker-comose

#step 3:create docker network

docker network create –driver=bridge main

#step 4:start container

cd docs

docker-compose scale superset=2 nginx=1

#step 5:visit

localhsot:80


