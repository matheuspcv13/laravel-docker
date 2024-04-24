
# Setup Docker Laravel 11 com PHP 8.3 e PostgresSQL
[Assine a Academy, e Seja VIP!](https://academy.especializati.com.br)

### Passo a passo
Clone Repositório
```sh
git clone -b laravel-11-with-php-8.3 https://github.com/matheuspcv13/laravel-docker.git nome_projeto
```
```sh
cd nome_projeto
```

Suba os containers do projeto
```sh
docker-compose up --build -d
```


Crie o Arquivo .env
```sh
cp .env.example .env
```

Acesse o container app
```sh
docker-compose exec app bash
```


Instale as dependências do projeto
```sh
composer install
```

Gere a key do projeto Laravel
```sh
php artisan key:generate
```


Rodar as migrations
```sh
php artisan migrate
```

### Possíveis erros com o banco

#### Connection refused
#### password authentication failed for user "postgres"

Acesse o container
```sh
cd caminho/do/projeto
docker-compose exec db psql -U postgres acf
```

Se não conseguir faça

```sh
sudo rm -rf ./.docker/postgresql/dbdata
```

Se conectou no db psql com usuario postgres possível que você se confundiu com as portas

Acesse o projeto
[http://localhost:8000](http://localhost:8000)
