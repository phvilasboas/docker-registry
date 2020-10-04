# docker-registry
Docker Hub privado


**1 - Subir o container do registry.**

_root@server:~# docker-compose up -d_

**1.1 - Adicionar os usuários para login**

_root@server:~# htpasswd -B auth/registry.passwd user_


**2 - Fazer proxy no apache**

copiar o arquivo registry-vhost.conf para o diretorio do apache.

Ajustar o arquivo registry-vhost.conf conforme dominio

_root@server:~# a2ensite registry-vhost.conf_

**3 - Fazer o restart do apache**

Para ver as imagens disponiveis no repositório, use:

http -a user https://repo.example.com.br/v2/_catalog
