
# WordPress in a Scalable Architecture
The project consists of provisioning multiple instances of WordPress in order to increase its scalability and availability. 
For this purpose, Nginx is used as a load balancer for the multiple WordPress instances.

## Instalation

**1 -**  Clone the repository:

    git clone https://github.com/vitorlima-dev/wordpress-lb.git

**2 -** Run the following command to start the services:
    
    docker-compose up
    
**3 -** Access WordPress at [http://localhost](http:localhost:80)

**4 -** After starting the five containers, run the following command a few times:
    
    curl -I http://<ip-do-host>/  

You will see that the X-Upstream HTTP header will display three possible IP addresses, which are the IPs of the WordPress containers.
These same addresses can also be verified in the browser by inspecting the page under the Network tab.

### A aquiterura que acabamos de provisionar fica assim !!

![Projeto Wordpress](https://github.com/vitorlima-dev/wordpress-lb/assets/131411785/eb4df95d-0aee-4a49-9e89-5ed08e4c23e3)



![nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![wordpress](https://img.shields.io/badge/WordPress-006E93?style=for-the-badge&logo=wordpress&logoColor=white)
![mysql](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)

