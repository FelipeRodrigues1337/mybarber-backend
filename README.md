- yarn
- Configurar novo arquivo .env
- Configurar banco de dados postgresql

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
- O prestador deve receber uma notificação sempre que houver um novo agendamento;
- O prestador deve poder visualizar as notificações não lidas

**RNF**
- Os agendamentos do prestador no dia devem ser armazenados em cache
- 
**RN**


# Agendamento de serviços

**RF**
- O usuário deve poder listar todos os prestadores de serviços cadastrados;
- O usuário deve poder listar os dias de um mês com pelo menos um horário disponível de um prestador;
- O usuário deve poder listar horários disponíveis em um dia específico de um prestador;
- O usuário deve poder realizar um novo agendamento com um prestador;
**RNF**
- A listagem de prestadores deve ser armazenada em cache;

**RN**
- Cada agendamento deve durar 1h exatamente;
- OS agendamentos devem estar disponíveis entre 8h ás 18h (Primeiro ás 8h, último ás 17h);
- O usuário não pode agendar em um horário já ocupado;
- O usuário não pode agendar em um horário que já passou;
- O usuário não pode agendar serviços consigo mesmo;
