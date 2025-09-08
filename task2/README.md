docker build -f ./Dockerfile -t softy-pinko-front-end:task2 .
docker run -p 9000:9000 -it --rm --name softy-pinko-front-end-task2 softy-pinko-front-end:task2


curl -I http://localhost:9000/
curl http://localhost:9000/ | head
