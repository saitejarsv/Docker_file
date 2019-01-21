docker run --name ubuntu1  -d ubuntu /bin/sh -c "while true; do ping 8.8.8.8; done"

docker run --name ubuntu2  -d ubuntu /bin/sh -c "while true; do ping 8.8.8.8; done"

create bridge network 
docker network create mybridge

docker run --name ubuntu3 --net=mybridge -d ubuntu /bin/sh -c "while true; do ping 8.8.8.8; done"

docker inspect ubuntu1 |grep -i ip

docker inspect ubuntu2 |grep -i ip

docker inspect ubuntu3 |grep -i ip

docekr exec ubuntu1 
ping ubuntu1 - works 
ping ubuntu3 - didnt work 

