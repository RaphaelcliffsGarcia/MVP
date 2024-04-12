# Projeto Python Full Stack

Este projeto é uma aplicação Python Full Stack que utiliza Next.js, Flask, PostgreSQL e Docker para criar um sistema composto por múltiplos componentes que se comunicam seguindo o padrão REST.

## Estrutura do Projeto

A estrutura do projeto é a seguinte:

```
projeto/
├── backend/
│   ├── app.py
│   ├── flask.dockerfile
│   └── ...
├── frontend/
│   ├── components/
│   │   ├── CardComponents.tsx
│   │   └── UserInterface.tsx
│   ├── next.dockerfile
│   └── ...
├── docker-compose.yml
└── README.md
```

## Tecnologias Utilizadas

- Python: 🐍
- Next.js 14: 🚀
- React: ⚛️
- Axios: 🌐
- Flask: 🌶️
- PostgreSQL: 🐘
- Docker: 🐳

## Funcionamento

⚙ Funcionamento: O front end, uma Single Page Application (SPA), consome informações da API fornecida pelo back end e lida com a interação da interface do usuário. O sistema foi construído utilizando componentes para facilitar o desenvolvimento paralelo por equipes distintas e oferece uma visão clara das interações entre as diferentes partes do sistema. Cada componente, incluindo o back end e o front end, é independente e pode ser desenvolvido, implantado e escalado de forma independente.

## Aplicativo Flask

O aplicativo Flask é responsável por fornecer uma API REST para interagir com os dados dos usuários. As interações com a API podem ser feitas utilizando o Postman ou ferramentas similares.

### Rotas da API Flask

1. **Criar um novo usuário:**
   - Método: POST
   - Rota: `/api/flask/users`
   - Corpo da solicitação (JSON):
     ```json
     {
         "username": "nome_do_usuario",
         "email": "email_do_usuario"
     }
     ```

2. **Obter todos os usuários:**
   - Método: GET
   - Rota: `/api/flask/users`

3. **Obter um usuário por ID:**
   - Método: GET
   - Rota: `/api/flask/users/{id}`
   - Substitua `{id}` pelo ID do usuário desejado.

4. **Atualizar as informações de um usuário:**
   - Método: PUT
   - Rota: `/api/flask/users/{id}`
   - Substitua `{id}` pelo ID do usuário que deseja atualizar.
   - Corpo da solicitação (JSON):
     ```json
     {
         "username": "novo_nome_do_usuario",
         "email": "novo_email_do_usuario"
     }
     ```

5. **Excluir um usuário:**
   - Método: DELETE
   - Rota: `/api/flask/users/{id}`
   - Substitua `{id}` pelo ID do usuário que deseja excluir.

## Utilizando o Postman

Para interagir com a API Flask, você pode utilizar o Postman ou qualquer outra ferramenta de teste de API.

1. Abra o Postman.

2. Insira o URL da API e selecione o método desejado (POST, GET, PUT, DELETE).

3. Adicione os parâmetros necessários e envie a solicitação.

## Requisitos

- Python 3.6 ou superior
- Flask
- Flask-SQLAlchemy
- Flask-Cors
- Docker (opcional, mas recomendado)

## Configuração

1. Clone este repositório:

```bash
git clone https://github.com/seu_usuario/seu_projeto.git
cd seu_projeto
```

2. Certifique-se de ter o Python e o pip instalados em seu sistema.

3. Instale as dependências do Flask:

```bash
pip install flask flask_sqlalchemy flask_cors
```

## Como Executar

### Sem Docker

1. No terminal, navegue até o diretório do projeto clonado.

2. Execute o seguinte comando para iniciar o aplicativo Flask:

```bash
python backend/app.py
```

### Com Docker

1. Certifique-se de ter o Docker instalado em seu sistema.

2. No terminal, navegue até o diretório do projeto clonado.

3. Execute o seguinte comando para construir e executar o contêiner Docker do aplicativo Flask:

```bash
docker build -t nome_imagem_flask -f backend/flask.dockerfile .
docker run -p 4000:4000 nome_imagem_flask
```

## Contribuição

Sinta-se à vontade para abrir issues ou enviar pull requests.


