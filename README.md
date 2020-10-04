# docker-registry
Docker Hub privado


**1 - Subir o container do registry.**

_root@home:~# docker-compose up -d_

**2 - Fazer proxy no apache**
copiar o arquivo registry-vhost.conf para o diretorio do apache.
Ajustar o arquivo registry-vhost.conf conforme dominio

_root@home:~# a2ensite registry-vhost.conf_

**3 - Fazer o restart do apache**

