# Docker-copy

docker cp [OPTIONS] CONTAINER:SRC_PATH DEST_PATH
docker cp [OPTIONS] SRC_PATH CONTAINER:DEST_PATH



docker cp mycontainer:/app/file.txt /home/user/


docker cp mycontainer:/app/data /home/user/


docker cp /home/user/data mycontainer:/app/


# Docker-exec
how to find out a file or folder inside a container

docker exec <container_name_or_id> sh -c "ls /path/to/folder"
docker exec mycontainer sh -c "ls /path/to/folder | grep myfile.txt"


how to list the path inside the container

docker exec <container_name_or_id> sh -c "ls"
docker exec mycontainer sh -c "ls /"
docker exec mycontainer sh -c "ls /app"


how to edit a file in a running container using exec option

docker exec -it 57700c1c2961 sh -c "apt-get update && apt-get install -y vim"
docker exec -it 57700c1c2961 vi /etc/pam.conf

docker exec -it mycontainer vi /path/to/myfile.txt
docker exec -it 57700c1c2961 sh -c "which vi"
