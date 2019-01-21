sudo apt-get update
sudo apt install docker.io -y
docker swarm init
sudo docker node ls
docker service create --replicas 5 -p 80:80 --name web nginx
sudo docker service  ps web
sudo docker service ls
docker service rm web
sudo docker service ls