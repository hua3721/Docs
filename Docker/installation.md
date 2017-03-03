__Linux__
* Red Hat
  * 1.Create a yum repo file: /etc/yum.repos.d/docker.repo. File content is as below:
  ```
       [docker]  
       name=Docker Repository  
       baseurl=https://yum.dockerproject.org/repo/main/centos/7  
       enabled=1  
       gpgcheck=1  
       gpgkey=https://yum.dockerproject.org/gpg  
       proxy=<proxy_url>  
       proxy_username:<proxy_username>
       proxy_password:<proxy_password>
```
  * 2.Install docker: 
        
       `$ yum install -y docker-engine`
   
  * 3.Finish up:
   
       `$ systemctl daemon-reload`  
       `$ systemctl start docker`  
       `$ systemctl enable docker` 
  
__Mac__
* Legacy solution: Docker toolbox
  * docker machine - tool to create and manage dockerized virtual host(i.e. with docker engine on it).
  * docker engine - consists of docker daemon(RESTFUL API) and docker client(CLI).
  * docker compose - tool to define and run application configuration(such as dockerfile)
  * VirtualBox
  * Installation directory: /usr/local/bin
* New solution:
  * [Mac app](https://docs.docker.com/docker-for-mac/)
  * HyperKit(not VirtualBox)
  * Manage VM directly(no docker machine)
  * Installation directory:/Applications

__Windows__
* Legacy solution: Docker toolbox
  * docker machine - tool to create and manage dockerized virtual host(i.e. with docker engine on it).
  * docker engine - consists of docker daemon(RESTFUL API) and docker client(CLI).
  * docker compose - tool to define and run application configuration(such as dockerfile)
  * VirtualBox
* New solution:
  * [Windows app](https://docs.docker.com/docker-for-windows/)