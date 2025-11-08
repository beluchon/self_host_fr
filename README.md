pas de débrideur ? ➡️ Teste Torbox ici : https://www.torbox.app/subscription?referral=5daecbad-00af-4e2d-af48-123ca49c1947

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
faite 

```
hostname -I
```

et copier la première ip

puis aller sur https://votre-ip:5001

une fois l'interface de dockge ouvert regarder https://github.com/beluchon/self_host_fr/blob/main/2%20nginx%20et%20cloudflare.md
