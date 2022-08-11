# Gênesis - Desafio de Código Laravel

Nesse teste serão cobrados alguns conceitos básicos abordado os seguintes tópicos:

* PHP (Laravel)
* CSS/HTML (Bootstrap)
* Jquery

O projeto em questão já possui a parte básica configurada, então não é necessário se preocupar com a configuração do Docker e Nginx.

Você irá desenvolver uma aplicação simples contendo apenas um caso de uso simples.

## Configuração da Máquina

- [Instale o Docker](https://docs.docker.com/get-docker/)


## Configuração do Desafio

- Use esse repositório como ponto de partida.
- Quando você terminar, lembre de fazer `push` em tudo e abrir um pull request.

## Rodando o projeto
Caso tenha problemas com a execuçao do docker, rode os comandos como usuario root ou adicione as devidas permissoes ao docker: https://docs.docker.com/engine/install/linux-postinstall/

```bash
docker-compose up -d --build
```

Rode o seguinte comando para fazer a instalação da pasta vendor:

docker exec -ti desafio-genesis-app composer install

```bash
docker exec -ti desafio-genesis-app composer install
```

Configure o arquivo .env
```bash
cp .env.example .env
```

Configure a chave do projeto:
```bash
docker exec -ti desafio-genesis-app php artisan key:generate
```

Para compilar o javascript rode os seguintes comandos, (nao e necessario instalar o node, pois no projeto está configurado um arquivo bash com a imagem do node), rode os comandos como usuário root:
```bash
./dnpm install
```

```bash
./dnpm run development
```

## Rodando o banco de dados

Utilizamos PostgreSQL como banco de dados principal, o banco de dados já está configurado, basta criar as migrações e rodar o comando:

Rode o comando migrate após criar suas migrações, lembre-se, as migrações não estado criadas, você deve fazê-las.

```bash
docker exec -ti desafio-genesis-app php artisan migrate
```

## O que você precisa entregar?

Uma mini aplicação que permite uma recepcionista agendar um atendimento para uma pessoa.

A página onde a pessoa entra (a página inicial do mini aplicativo) já é a página para realizar o agendamento.

O fluxo de agendamento deve seguir os seguintes passos:


1. Tela inicial com botão de criar novo agendamento e listagem de agendamentos existentes
2. Tela de criar agendamento, contém os seguintes campos  
   1. Nome
   2. CPF
   3. Cartao SUS
   4. Motivo do atendimento
   5. Data do atendimento
   6. Urgência do atendimento (baixa, media, alta, urgente)
   7. Médico atendente
   8. Profissional que realizou o agendamento
3. Após o cadastro do agendamento o usuário é redirecionado para a tela inicial, onde pode ver a listagem dos agendamentos
4. O usuário deve ter a possibilidade de editar o agendamento
5. Não deve ser possível a criação de agendamentos no mesmo horário, e  nem o reagendamento ( edição ) de um agendamento em um horário existente
6. A tabela que irá os agendamentos deve conter todos os campos citados na etapa 2

Esperamos que você entregue os 6 passos acima em uma experiência para a pessoa que deseja realizar um agendamento de um paciente.

Seja criativo!

## Regras de Implementação

- Explique suas ideias como comentários no código; Fique a vontade para usar Português ou Inglês.

## Importante

- Caso tenha dúvidas, faça perguntas pontuais para dar continuidade ao desafio
- A parte mais importante do mini projeto e o laravel, caso tenha dúvidas relacionados ao jquery sinta-se livre para fazer perguntas

# liveware-demo
