cd ~/holberton/holbertonschool-softy-pinko-docker
docker build -f task0/Dockerfile -t softy-pinko:task0 task0
docker run -it --rm --name softy-pinko-task0 softy-pinko:task0
