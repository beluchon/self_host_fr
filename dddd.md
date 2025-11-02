installer ubuntu server ou le lancer via votre vps

ps: n'oublier rien de 
<img width="1272" height="319" alt="2025-11-02 11_42_16-Ubuntu 64-bit - VMware Workstation" src="https://github.com/user-attachments/assets/bc57bfda-c04a-4f7c-8aa1-a990f4adb1a6" />

installer open ssh

faire:

sudo apt update
sudo apt upgrade -y

pour docker:

sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

puis

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

sudo systemctl status docker
vous aurrai une interface faire Q pour en sortir
