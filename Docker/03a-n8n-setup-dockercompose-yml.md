if you dont have docker-compose.yml make it with  
  
1. In WSL, go to your project folder:
`
mkdir ~/n8n && cd ~/n8n
`  
  
2. Create the file:  
`
nano docker-compose.yml
`  
  
3. Paste the YAML script  
```
version: "3.8"

services:
  n8n:
    image: n8nio/n8n
    container_name: n8n
    restart: unless-stopped
    ports:
      - "5678:5678"
    environment:
      - N8N_BASIC_AUTH_ACTIVE=true
      - N8N_BASIC_AUTH_USER=myemail@example.com
      - N8N_BASIC_AUTH_PASSWORD=newpassword123
    volumes:
      - n8n_data:/home/node/.n8n

volumes:
  n8n_data:
    driver: local
```  
  
4. launch n8n again:
`
docker-compose up -d
`  
-d runs it in the background.  
The container will restart automatically if your machine reboots.  
  
#### < [Back](./03-n8n.md) 