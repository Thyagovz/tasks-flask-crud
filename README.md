# API de Gerenciamento de Tarefas

## Descrição

API REST desenvolvida em Flask para gerenciamento de tarefas (To-Do List). Este projeto implementa operações CRUD (Create, Read, Update, Delete) permitindo criar, visualizar, atualizar e deletar tarefas de forma eficiente.

## Tecnologias Utilizadas

- Python
- Flask
- Pytest (para testes)
- Requests
- Werkzeug

## Funcionalidades

- Criar nova tarefa
- Listar todas as tarefas
- Buscar tarefa específica por ID
- Atualizar tarefa existente
- Deletar tarefa
- Sistema de controle de IDs automático
- Suporte a descrições opcionais nas tarefas

## Rotas da API

### POST /tasks

- Cria uma nova tarefa
- Corpo da requisição deve conter título e descrição (opcional)
- Retorna ID da tarefa criada

### GET /tasks

- Lista todas as tarefas cadastradas
- Retorna array de tarefas e total de tarefas

### GET /tasks/{id}

- Busca uma tarefa específica pelo ID
- Retorna detalhes da tarefa ou 404 se não encontrada

### PUT /tasks/{id}

- Atualiza uma tarefa existente
- Corpo da requisição deve conter título, descrição e status de conclusão
- Retorna mensagem de sucesso ou 404 se não encontrada

### DELETE /tasks/{id}

- Remove uma tarefa específica
- Retorna mensagem de sucesso ou 404 se não encontrada

## Estrutura das Tarefas

Cada tarefa possui os seguintes campos:

- `id`: Identificador único da tarefa (automático)
- `title`: Título da tarefa (obrigatório)
- `description`: Descrição detalhada (opcional)
- `completed`: Status de conclusão (booleano)

## Configuração do Ambiente

1. Clone o repositório:

```bash
git clone https://github.com/Thyagovz/tasks-flask-crud.git
cd tasks-flask-crud
```

2. Crie um ambiente virtual:

```bash
python -m venv venv
```

3. Instale as dependências:

```bash
pip install -r requirements.txt
```

4. Execute a aplicação:

```bash
python app.py
```

A API estará disponível em `http://localhost:5000`

## Testes

Para executar os testes da aplicação:

```bash
pytest tests.py
```
