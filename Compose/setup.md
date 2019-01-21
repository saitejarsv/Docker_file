sudo curl -L "https://github.com/docker/compose/releases/download/1.23.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version

Commands - 

docker-compose up 
docker-compose up -d
docker-compose ps
docker-compose down
docker-compose scale web=2