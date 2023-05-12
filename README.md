
# Wordpress em uma Arquitetura Escalável
O projeto consiste em provisionar múltiplas instâncias do Wordpress,
de modo a aumentar sua escalabilidade e disponibilidade. Para isso, é utilizado o 
Nginx como balanceador de carga para as múltiplas instâncias do Wordpress.

## Instalação

**1 -**  Clone o repositório :

    git clone https://github.com/vitorlima-dev/wordpress-lb.git

**2 -** Digite o comando abaixo para inicializar os serviços :
    
    docker-compose up
    
**3 -** Acesse o wordpress em [http://localhost](http:localhost:80)

**4 -** Após iniciar os cinco contêineres, execute algumas vezes o comando 
    
    curl -I http://<ip-do-host>/  

Veja que o cabeçalho HTTP X-Upstream irá assumir três possíveis endereços de IP, que são os IPs dos contêineres do Wordpress. 
Os mesmo endereços podem ser verificados via navegador, inspecionando a página, na aba Rede.

### A aquiterura que acabamos de provisionar fica assim !!

![Projeto Wordpress](https://github.com/vitorlima-dev/wordpress-lb/assets/131411785/eb4df95d-0aee-4a49-9e89-5ed08e4c23e3)



![nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![wordpress](https://img.shields.io/badge/WordPress-006E93?style=for-the-badge&logo=wordpress&logoColor=white)
![mysql](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)

