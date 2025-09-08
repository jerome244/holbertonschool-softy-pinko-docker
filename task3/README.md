cd ~/holberton/holbertonschool-softy-pinko-docker/task3
docker build -f ./back-end/Dockerfile -t softy-pinko-back-end:task3 ./back-end
docker run -p 5252:5252 -it --rm --name softy-pinko-back-end-task3 softy-pinko-back-end:task3




Sanity check (new terminal):

curl http://localhost:5252/api/hello
# Hello, World!






Terminal 2 — front-end
cd ~/holberton/holbertonschool-softy-pinko-docker/task3
docker build -f ./front-end/Dockerfile -t softy-pinko-front-end:task3 ./front-end
docker run -p 9000:9000 -it --rm --name softy-pinko-front-end-task3 softy-pinko-front-end:task3