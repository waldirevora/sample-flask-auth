# sample-flask-auth

# API de Autenticação com Flask

Projeto prático desenvolvido durante o curso de Python com Flask da **Rocketseat**.

O objetivo foi aprender a construir uma API utilizando Flask, implementar autenticação de usuários, trabalhar com rotas HTTP e integrar uma aplicação Python a um banco de dados.

## Funcionalidades

- Cadastro de usuários.
- Login e logout utilizando Flask-Login.
- Gerenciamento de sessões.
- Consulta de usuários cadastrados.
- Atualização de senha.
- Exclusão de usuários.
- Persistência de dados com SQLite e SQLAlchemy.
- Proteção de rotas que exigem autenticação.

## Tecnologias utilizadas

- Python
- Flask
- Flask-Login
- Flask-SQLAlchemy
- SQLite

## Estrutura do projeto

- `app.py`: configuração da aplicação, autenticação e rotas da API.
- `database.py`: configuração do SQLAlchemy.
- `models/user.py`: modelo de dados do usuário.
- `requirements.txt`: dependências do projeto.

## Como executar

**1. Clone o repositório:**

`git clone https://github.com/waldirevora/sample-flask-auth.git`

**2. Acesse a pasta:**

`cd sample-flask-auth`

**3. Crie um ambiente virtual:**

`python -m venv .venv`

Ative o ambiente virtual:

Windows (PowerShell):

`.\.venv\Scripts\Activate.ps1`

Linux/macOS:

`source .venv/bin/activate`

**4. Instale as dependências:**

`pip install -r requirements.txt`

**5. Inicialize o banco de dados:**

Execute:

`flask --app app shell`

Dentro do shell do Flask:

`from database import db`

`db.create_all()`

`exit()`

**6. Inicie a aplicação:**

`python app.py`

A API estará disponível localmente em:

`http://127.0.0.1:5000`

## Rotas disponíveis

| Método | Endpoint          | Descrição              |
| ------ | ----------------- | ---------------------- |
| GET    | `/hello`          | Rota de teste          |
| POST   | `/user`           | Cadastro de usuário    |
| POST   | `/login`          | Autenticação           |
| GET    | `/logout`         | Encerramento da sessão |
| GET    | `/user/<id_user>` | Consulta de usuário    |
| PUT    | `/user/<id_user>` | Atualização de senha   |
| DELETE | `/user/<id_user>` | Exclusão de usuário    |

As rotas de consulta, atualização, exclusão e logout exigem autenticação.

### Exemplo de cadastro

Endpoint: `POST /user`

Corpo da requisição (JSON):

```json
{
  "username": "usuario_teste",
  "password": "senha_teste"
}
```

O mesmo formato de dados é utilizado na rota de login.

## Observações

Este repositório representa um exercício de aprendizagem e não uma implementação pronta para produção.

O código original ainda precisa de melhorias de segurança, como armazenamento de senhas com hash, configuração da chave secreta por variável de ambiente, validação de permissões e tratamento de erros.

## Formação

**Rocketseat**  
Curso de Python com Flask
