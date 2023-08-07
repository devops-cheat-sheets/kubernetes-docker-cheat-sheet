# Kubernetes and Docker

 
### Kubernetes Commands Cheat Sheet



Here is a cheat sheet of 20 frequently used Kubernetes commands, along with a detailed explanation for each of them. 

Command | Explanation
--------|-------------
`kubectl get nodes` | List all nodes in the cluster.
`kubectl get pods` | List all pods in the default namespace.
`kubectl get pods -n my-namespace` | List all pods in a specific namespace.
`kubectl get pods -o jsonpath={.items[*].metadata.name}` | List the names of all pods using jsonpath. 
`kubectl describe node my-node` | Detailed information about a specific node.
`kubectl describe pod my-pod` | Detailed information about a specific pod.
`kubectl logs my-pod` | Print the logs for a specific pod.
`kubectl exec my-pod -- date` | Execute a command in a specific pod (e.g., print current date).
`kubectl run my-pod --image=my-image` | Run a specific image in a new pod.
`kubectl delete pod my-pod` | Delete a specific pod.
`kubectl create -f my-config.yaml` | Create resources defined in a specific YAML file.
`kubectl apply -f my-config.yaml` | Apply changes to resources defined in a specific YAML file.
`kubectl delete -f my-config.yaml` | Delete resources defined in a specific YAML file.
`kubectl get services` | List all services in the default namespace.
`kubectl get services -n my-namespace` | List all services in a specific namespace.
`kubectl get deployments` | List all deployments in the default namespace.
`kubectl get deployments -n my-namespace` | List all deployments in a specific namespace.
`kubectl scale --replicas=3 deployment/my-deployment` | Scale a deployment to 3 replicas.
`kubectl rollout status deployment/my-deployment` | Check the rollout status of a specific deployment.
`kubectl rollout undo deployment/my-deployment` | Roll back the last update to a specific deployment.

These are common commands that will help you manage your Kubernetes cluster. Please consult the Kubernetes documentation for a more detailed list and for commands specific to your use case.


### Docker Commands Cheat Sheet



Command | Explanation
--------|-------------
`docker run image` | Run a Docker container from an image.
`docker run -it image` | Run an image in interactive mode with a terminal attached.
`docker run -d image` | Run an image in the background (detached mode).
`docker run -p 8080:80 image` | Run an image and map host port 8080 to container port 80.
`docker run -v /host/dir:/container/dir image` | Run an image with a host directory mounted into the container.
`docker ps` | List all running Docker containers.
`docker ps -a` | List all Docker containers, both running and stopped.
`docker stop container_id` | Stop a running Docker container.
`docker rm container_id` | Remove a Docker container.
`docker rmi image` | Remove a Docker image.
`docker images` | List all Docker images.
`docker pull image` | Pull a Docker image from a registry.
`docker push image` | Push a Docker image to a registry.
`docker build -t image .` | Build a Docker image from a Dockerfile in the current directory.
`docker exec -it container_id command` | Execute a command in a running Docker container.
`docker logs container_id` | Get the logs from a Docker container.
`docker network ls` | List all Docker networks.
`docker volume ls` | List all Docker volumes.
`docker login` | Log in to a Docker registry.
`docker tag image new_tag` | Tag a Docker image with a new tag.
`docker history image` | Show the history of an image, including the commands that were run to build it.
`docker inspect container_id` | Display detailed information in JSON format for a running container.
`docker search term` | Search the Docker Hub for images.
`docker save -o file.tar image` | Save an image to a tar archive.
`docker load -i file.tar` | Load an image from a tar archive.
`docker top container_id` | Display the running processes in a container.
`docker diff container_id` | Show file system changes in a container.
`docker cp container_id:/file/path /host/path` | Copy files/folders from a container to the host.
`docker commit container_id new_image` | Create a new image from a container's changes.
`docker port container_id` | Show port mapping for a container.
`docker stats container_id` | Show a live stream of container(s) resource usage statistics.
`docker wait container_id` | Block until a container stops, then print its exit code.
`docker update container_id` | Update configuration of one or more containers.
`docker system df` | Display detailed information on space usage within Docker.
`docker system prune` | Remove all unused Docker objects.
`docker container ls` | List all running containers. Similar to `docker ps`.
`docker container rm container_id` | Remove one or more containers. Similar to `docker rm`.
`docker image ls` | List all images. Similar to `docker images`.
`docker image rm image_id` | Remove one or more images. Similar to `docker rmi`.
`docker network create network_name` | Create a new network.
`docker volume create volume_name` | Create a new volume.
`docker network connect network_name container_id` | Connect a network to a container.
`docker network disconnect network_name container_id` | Disconnect a network from a container.
`docker volume inspect volume_name` | Display detailed information on a specific volume.
`docker image inspect image_name` | Display detailed information on a specific image.
`docker container start container_id` | Start one or more stopped containers.
`docker container stop container_id` | Stop one or more running containers.
`docker container pause container_id` | Pause all processes within one or more containers.
`docker container unpause container_id` | Unpause all processes within one or more containers.
`docker container restart container_id` | Restart one or more containers.
`docker container kill container_id` | Kill one or more running containers.
`docker container attach container_id` | Attach local standard input, output, and error streams to a running container.
`docker container prune` | Remove all stopped containers.
`docker image prune` | Remove unused images.
`docker container export container_id -o file.tar` | Export a container's filesystem as a tar archive.
`docker container commit container_id` | Create a new image from a container's changes.
`docker container rename old_name new_name` | Rename a container.
`docker container run -it --rm --name container_name image` | Run a command in a new container, interactively, remove the container when it stops, and name it.
`docker container exec -it container_id command` | Run a command in a running container, interactively.
`docker buildx build --platform linux/amd64,linux/arm64 -t image .` | Build an image for multiple platforms using buildx.
`docker buildx ls` | List builder instances.
`docker buildx use builder_name` | Set the current builder instance.
`docker buildx create --use` | Create a new builder instance and switch to it.
`docker buildx inspect --bootstrap` | Inspect current builder instance.
`docker buildx rm builder_name` | Remove a builder instance.
`docker node ls` | List nodes in a swarm.
`docker swarm init` | Initialize a swarm.
`docker stack ls` | List stacks.
`docker stack deploy -c docker-compose.yml stack_name` | Deploy a new stack or update an existing stack.
`docker stack rm stack_name` | Remove a stack.
`docker secret ls` | List secrets.
`docker secret create secret_name secret_data` | Create a secret from a file or STDIN as a single string.
`docker secret rm secret_name` | Remove one or more secrets.
`docker service create --name service_name image` | Create a new service.
`docker service ls` | List services.
`docker service rm service_name` | Remove one or more services.
`docker service scale service_name=num_replicas` | Scale one or multiple replicated services.
`docker service update service_name` | Update a service.
`docker service ps service_name` | List the tasks of one or more services.
`docker service logs service_name` | Fetch the logs of a service or task.
`docker config ls` | List configs.
`docker config create config_name file` | Create a config from a file or STDIN.
`docker config rm config_name` | Remove one or more configs.
`docker plugin ls` | List plugins.
`docker plugin install plugin_name` | Install a plugin.
`docker plugin rm plugin_name` | Remove one or more plugins.
`docker plugin enable plugin_name` | Enable a plugin.
`docker plugin disable plugin_name` | Disable a plugin.
`docker checkpoint ls container_id` | List checkpoints.
`docker checkpoint create container_id checkpoint_name` | Create a checkpoint.
`docker checkpoint rm container_id checkpoint_name` | Remove a checkpoint.
`docker system info` | Display system-wide information.
`docker system events` | Get real time events from the server.
`docker trust signer add --key signer_pub_key.pem signer_name repo/image` | Add a signer for a repository or image.
`docker trust revoke repo/image` | Revoke a signed tag.
`docker trust inspect --pretty repo/image` | Return detailed information about signatures for images.
`docker login [options] [server]` | Log in to a Docker registry server.
`docker logout [server]` | Log out from a Docker registry server.
`docker manifest create list image[:tag] [image[:tag] ...]` | Create a local manifest list for annotating and pushing to a registry.
`docker manifest inspect image[:tag]` | Display an image's manifest, or a local or remote manifest list.
`docker manifest push [options] name[:tag]` | Push a manifest list or image index to a registry.
`docker manifest annotate name[:tag] image[:tag] [options]` | Add additional information to a local image manifest or manifest list.
`docker network prune` | Remove all unused networks.
`docker volume prune` | Remove all unused volumes.
`docker image save image -o file.tar` | Save one or more images to a tar archive.
`docker image load -i file.tar` | Load an image or repository from a tar archive.
`docker image prune -a` | Remove all unused images, not just dangling ones.
`docker container port container_id` | List port mappings for the container, or specify a specific mapping.
`docker container diff container_id` | Inspect changes to files or directories on a container's filesystem.
`docker container top container_id` | Display the running processes of a container.
`docker container stats [container_id...]` | Display a live stream of container(s) resource usage statistics.
`docker container exec -it container_id command` | Run a command in a running container.
`docker network create -d driver_name network_name` | Create a network with a specified driver.
`docker network rm network_id` | Remove one or more networks.
`docker network connect network_id container_id` | Connect a network to a container.
`docker network disconnect network_id container_id` | Disconnect a network from a container.
`docker volume create volume_name` | Create a volume.
`docker volume rm volume_name` | Remove one or more volumes.
`docker volume inspect volume_name` | Display detailed information on a specific volume.
`docker volume prune` | Remove all unused local volumes.
`docker node update --availability drain node_id` | Update a node's status to 'drain' to prepare for maintenance.
`docker node demote node_id` | Demote one or more nodes from manager in the swarm.
`docker node promote node_id` | Promote one or more nodes to manager in the swarm.
`docker swarm leave --force` | Force swarm to leave even if it is the last manager or that it will break the cluster.
`docker swarm join-token worker` | Show join command for worker.
`docker swarm join-token manager` | Show join command for manager.


