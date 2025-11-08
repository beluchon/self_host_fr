docker

```# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
docker compose

```# Add Docker's official GPG key:
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
lancer aux démarrage docker

```# Add Docker's official GPG key:
sudo systemctl start docker
```

puis dockge

```
sudo mkdir -p /opt/stacks /opt/dockge
sudo cd /opt/dockge

sudo curl https://raw.githubusercontent.com/louislam/dockge/master/compose.yaml --output compose.yaml

sudo docker compose up -d

sudo docker-compose up -d
```

puis aller sur https://votre-ip:5001
