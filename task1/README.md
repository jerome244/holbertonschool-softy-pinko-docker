# from task1 directory
docker build -t softy-pinko:task1 .
docker run -p 5252:5252 -it --rm --name softy-pinko-task1 softy-pinko:task1


You should see lines like:

 * Running on http://127.0.0.1:5252
 * Running on http://172.17.0.2:5252



In another terminal:

curl http://localhost:5252/api/hello
# -> Hello, World!