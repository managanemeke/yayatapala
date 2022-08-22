# yayatapala

Simple Yii2 docker-compose template
with builtin Apache, MySQL, phpMyAdmin
to make easy start on basic app development distance.

## Golden way installation on Ubuntu 20.04 blank server

### installapps stage

- `apt update`  
    `apt install ca-certificates curl gnupg lsb-release`  
    `mkdir -p /etc/apt/keyrings`  
    `curl -fsSL 
    https://download.docker.com/linux/ubuntu/gpg | 
    sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg`  
    `echo 
    "deb [arch=$(dpkg --print-architecture) 
    signed-by=/etc/apt/keyrings/docker.gpg] 
    https://download.docker.com/linux/ubuntu 
    $(lsb_release -cs) stable" | 
    sudo tee /etc/apt/sources.list.d/docker.list > 
    /dev/null`  
    `apt update`  
    `apt install docker-ce docker-ce-cli 
    containerd.io docker-compose-plugin`  
- `curl -L 
  "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" 
  -o /usr/local/bin/docker-compose`  
    `chmod +x /usr/local/bin/docker-compose`  

### configapps stage

- `cd ~`  
    `rm -r yayatapala`  
    `git clone https://github.com/managanemeke/yayatapala`  
    `cd yayatapala`

### startapps stage

- `./ma.sh`

### testapps stage

- `docker --version`  
    `docker-compose --version`

- `wget http://localhost:8080`  
    `vi index.html`  
    and you will see...

### stopapps stage

- `./na.sh`

