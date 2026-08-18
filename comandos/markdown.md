---
title: "Sistema de Sustentação ICMBio"
author: "Igor Barros"
---

# Sistema de Integração ICMBio

![Build](https://img.shields.io/badge/build-passing-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)

## Descrição
Sistema responsável pela integração de dados ambientais entre bases PostgreSQL e serviços externos.

## Tecnologias
- PHP 8.2 / Laravel 10
- PostgreSQL + PostGIS
- Docker / Kubernetes
- GitLab CI/CD

## Instalação

​```bash
git clone https://github.com/icmbio/sistema.git
cd sistema
composer install
cp .env.example .env
php artisan key:generate
​```

## Configuração do Banco de Dados

​```env
DB_CONNECTION=pgsql
DB_HOST=127.0.0.1
DB_DATABASE=icmbio
DB_USERNAME=postgres
DB_PASSWORD=secret
​```

## Uso

​```bash
php artisan migrate --seed
php artisan serve
​```

## Endpoints da API

| Método | Rota          | Descrição              |
|--------|---------------|-------------------------|
| GET    | `/api/areas`  | Lista áreas protegidas |
| POST   | `/api/areas`  | Cria nova área          |

## Testes

​```bash
php artisan test
​```

## Roadmap
- [x] Migração inicial do banco
- [x] Autenticação via API
- [ ] Integração com PostGIS
- [ ] Dashboard Power BI

<details>
<summary>Ver log de erro comum</summary>

​```
SQLSTATE[42P01]: Undefined table: relation "areas" does not exist
​```

Solução: rode `php artisan migrate` antes de iniciar o servidor.

</details>

## Licença
Distribuído sob licença MIT.
