# Preparando ambiente

**Exemplo de comandos para criar imagens Docker:**

- docker run -d --name postgre -e POSTGRESQL_PASSWORD=**** -e POSTGRESQL_USERNAME=**** -e POSTGRESQL_DATABASE=*** -p ****:5432 bitnami/postgresql:latest

- docker run -d --name mongodb -e MONGODB_USERNAME=**** -e MONGODB_PASSWORD=**** -e MONGODB_ROOT_PASSWORD=**** -e MONGODB_DATABASE=**** -p ****:27017 bitnami/mongodb:latest

- docker run -d --name redis -e REDIS_PASSWORD=**** -p ****:6379 bitnami/redis:lates


**Configurar Projeto:**
 - Instalar node 14.15.4 e yarn 1.22.5
 
 - Instalar dependências: yarn

 - Configure um novo arquivo ormconfig.json a partir do ormconfig.example.json de acordo com os bancos criados

 - Configure um novo arquivo .env a partir do env.example
	
 - Execute: ./node_modules/.bin/typeorm migration:run

 - Execute: yarn build
	
 - Rodar projeto: yarn dev:server

# Recuperação de senha
**RF**
 - O usuário deve poder recuperar sua senha informando o seu e-mail;

 - O usuário deve receber um e-mail com instruções de recuperação de senha;

 - O usuário deve poder resetar sua sneha;
**RNF**

- Utilizar Mailtrap para testar envios em ambiente de dev;

- Utilizar Amazon SES para envios em produção;

- O envio de e-mails deve acontecer em segundo plano (background);

**RN**
- O link enviado por email para resetar senha, deve expirar em 2h;

- O usuário precisa confirmar a nova senha ao resetar sua senha;

# Atualização do perfil
**RF**

- O usuário deve poder atualizar seu nome, email e senha;

**RN**
- O usuário não pode alterar seu email para um email já utilizado;
- Para atualizar sua senha, o usuário deve informar a senha antiga;
- Para atualizar sua senha, o usuário precisa confirmar sua senha;

# Painel do prestador

**RF**
- O usuário deve poder listar seus agendamentos de um dia específico;
**RNF**
- Os agendamentos do prestador no dia devem ser armazenados em cache
**RN**

# Rotas
https://docs.google.com/document/d/13afKsjuedM1N7Vi61lxL3PrJZJr8DUfC2Tm9-YzU0mQ/edit?usp=sharing
