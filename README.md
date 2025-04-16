# Docker-Installation
How to install docker in VPS/Ubuntu
Update your packages: sudo apt update && sudo apt upgrade -y
Install dependencies: sudo apt install -y ca-certificates curl gnupg lsb-release
Add Docker’s GPG key: sudo mkdir -p /etc/apt/keyrings && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
Set up the Docker repository: echo \ "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] \https://download.docker.com/linux/ubuntu \ $(lsb_release -cs) stable" | \ sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
Install Docker Engine: sudo apt update && sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
Verify Docker installation: sudo docker run hello-world
(Optional) Allow running Docker without sudo: sudo usermod -aG docker $USER && newgrp docker
