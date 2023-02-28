# DOCKER PARA A LARAVEL APP

## Descrição

Laravel app:

- Php 8.1
- Nginx
- MySql
- PhpMyadmin
- redis
- Node.js 18.x

## STEPS PARA BUILD APP

1. Abra o terminal (WSL2)

```sh
Rode o docker dentro do terminal WSL2
```

2. Clone Repositório

```sh
git clone https://github.com/GabrielMBoeira/setup-laravel-docker my-project
```

3. Acesse o diretório criado

```sh
cd my-project/
```

4. Remova o versionamento

```sh
rm -rf .git/
```

4. Crie o Arquivo .env
```sh
cp .env.example .env
```

5. Somente rode este comando caso não tenha acesso docker ubuntu

```sh
sudo chmod 666 /var/run/docker.sock

sudo chmod 775 -R mysql (permissão no diretório mysql)

sudo chown -R "${USER:-$(id -un)}" . 
```

6. crie as imagens 

```sh
docker-compose build
```

7. Suba os containers do projeto

```sh
docker-compose up -d
```

8. Acesse o container app com o bash

```sh
docker-compose exec app bash
```

9. Instale as dependências do projeto

```sh
composer install
```

10. Gere a key do projeto Laravel

```sh
php artisan key:generate
```

11. Configure o arquivo .gitignore

```sh
Informar arquivo .env e arquivos DB
```

Acesse o projeto
[http://localhost](http://localhost)
