# superset_deploy
Deploy for superset

#step 1:get resource

git clone https://github.com/tddv/superset_deploy.git

#step 2:install docker-compose
 
apt-get update 

apt-get install python-pip

pip uninstall docker-compose

pip install docker-comose

#step 3:start container
docker-compose scale superset=2 nginx=1

#step 4:visit
localhsot:80

