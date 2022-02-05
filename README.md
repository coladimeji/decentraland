Decentralised
step 1. Create a foler
Open your terminal
mkdir my_decentralised
cd my_decentralised

NOTE: since am using MAC I will be using Homebrew to install docker

Step 2.brew install docker
NOTE: Check for docker version example docker -v


$ sudo apt-get update



$ sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg

$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

$  echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

$ sudo apt-get update

$ sudo apt-get upgrade

$ sudo apt-get install docker-ce docker-ce-cli containerd.io


Step 3. Install Docker-Compose

$ sudo curl -L "https://github.com/docker/compose/releases/download/1.28.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

$ sudo chmod +x /usr/local/bin/docker-compose

Step 4. Add $USER to Docker Group

$ sudo groupadd docker

$ sudo usermod -aG docker $USER

$ newgrp docker

Step 5. Verify Docker Install

$ docker run hello-world

Step 6. Verify Docker-Compose Install

$ docker-compose --version
docker-compose version 1.28.5, build c4e3a1f

Step 7. Stop Apache2

$ sudo systemctl disable apache2 && sudo systemctl stop apache2

Step 8. Install Git

$ sudo apt-get update

$ sudo apt-get install git

Step 9. Create Directory for Catalyst Source Code

$ mkdir catalyst

$ cd catalyst

Step 10. Download Catalyst-Owner from Decentraland's Github

$ git clone https://github.com/decentraland/catalyst-owner  

Step 11. Delete .example extensions from environment files

$ mv .env.example .env

$ mv .env-advanced.example .env-advanced

Step 12. Edit Environment File

$ nano .env

# Configuration to be set by node owners
EMAIL=coladimeji@gmail.com
CONTENT_SERVER_STORAGE=./storage
CATALYST_URL=http://localhost:8080

Step 13. Create Storage Folder

$ mkdir storage

Step 14. Run Catalyst Server

$ ./init.sh

Final message to confirm that the server is functioning:

## Catalyst server is up and running at http://localhost:8080

Please let me know if you were able to successfully follow these steps and any bumps you may have encountered along the way.

Your turn to support the network!
