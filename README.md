# GLPI no Ubuntu server 22.04 LTS

Repositorio de instalação do GLPI no Ubuntu server 22.04 LTS
 
## Instalação do Docker e Docker Compose

### Docker

```bash
curl -fsSL https://get.docker.com | sh
```
### Docker Compose

```bash
curl -L https://github.com/docker/compose/releases/download/1.25.1/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
```

## Instalação GlPI

### Criação das pastas no Ubuntu

```bash
cd opt

git clone https://github.com/G4briel0ss/glpi.git

cd glpi

mkdir -p ./var/www/html/glpi \ ./var/lib/mysql

chown 472:472 ./var/lib/mysql \ ./var/lib/mysql 
```
### Executando os containers

```bash
docker compose up -d
```

### Acessando o GlPI

https://server-ip

### Finalizando a instalação 

> selecionar o idioma

> Clique em Install

### Conectando com o banco de dados

SQL server
> MySql

SQL User
> glpi_user

SQL password
> glpi

### Escolha do database

selecione o glpidb

- [x] glpidb
- [ ] Cria um novo banco de dados 

### Os usuários e senhas padrões são:

| User/pass | Description |
| --- | --- |
| glpi/glpi | para a conta do usuário administrador |
| tech/tech | para a conta do usuário técnico |
| normal/normal | para a conta do usuário normal |
| post-only/postonly | para a conta do usuário postonly |

> [!IMPORTANT]
> *Por padrão devemos alterarmos as senhas padrões*.


