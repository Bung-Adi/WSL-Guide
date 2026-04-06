#### run these if needed for a user runing docker  
`sudo usermod -aG docker $USER`  

#### force Debian to recognize your new group membership right now  
`newgrp docker`

#### to start docker  
`sudo service docker start`
and or if needed to start
`sudo /etc/init.d/docker start`

#### to check if started  
`docker ps`