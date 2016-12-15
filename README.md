# superset_deploy
Deploy for superset

step 1:
git clone https://github.com/tddv/superset_deploy.git

step 2:
# install docker-compose
apt-get update
apt-get install python-pip
pip uninstall docker-compose
pip install docker-comose

step 3:
docker-compose scale superset=2 nginx=1

step 4:
type localhost:80 in your browser

