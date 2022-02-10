# Session-2
In this session we are talking about some AWS essential services for our app architecture, best practices, containers and how to manage them.

## Configuration

### Docker
1. Search the Docker number on the Amazon Linux Extra packages:
> sudo amazon-linux-extras list
2. In my case the number it is 20, install it:
> sudo amazon-linux-extras install 20
3. Enable the Docker daemon:
> sudo systemctl start docker
4. Pull some images:
> sudo docker pull some:images

### Docker Compose
1. Download the Docker compose package:
>  sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
2. Apply executable permissions to the binary:
> sudo chmod +x /usr/local/bin/docker-compose
3. Test the installation:
> docker-compose --version

### AWS CLI
1. Configure AWS CLI:
> sudo aws configure

### Minikube
1. Check the architecture of your current server:
> uname -a
2. Go and check Minikube documentation about how to dowload your right package, in my case was this way:
```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-amd64
sudo install minikube-darwin-amd64 /usr/local/bin/minikube
```
3. Create and start a Minikube cluster:
> minikube start --driver docker

4. Check Minikube status:
> minikube status
