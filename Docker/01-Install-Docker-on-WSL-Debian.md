#### Dont forget to update  
`sudo apt update && sudo apt upgrade -y`  

#### 1. Install helper first  
`sudo apt install ca-certificates curl gnupg lsb-release -y`  

#### 2. Create Keyring folder  
`sudo mkdir -p -m 0755 /etc/apt/keyrings`  

#### 3. Download gpg  
`sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.gpg`  

#### 4. Veryfied  
`ls -l /etc/apt/keyrings/docker.gpg`  
If it says "No such file," the download failed.  

#### 5. Grand permision to key  
`sudo chmod a+r /etc/apt/keyrings/docker.gpg`  

#### 6. Update  
`sudo apt update`  

#### 7. Install  
`sudo apt install docker-ce docker-ce-cli containerd.io docker-compose-plugin -y`  