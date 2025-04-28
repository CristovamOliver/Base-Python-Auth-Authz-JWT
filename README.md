# Exemplo de Autenticação JWT com FastAPI

Este é um exemplo de implementação de autenticação e autorização usando JWT (JSON Web Tokens) com FastAPI.

## Instalação

1. Crie um ambiente virtual:
```bash
python -m venv venv
```

2. Ative o ambiente virtual:
- Windows:
```bash
.\venv\Scripts\activate
```
- Linux/Mac:
```bash
source venv/bin/activate
```

3. Instale as dependências:
```bash
pip install -r requirements.txt
```

## Executando a API

```bash
uvicorn main:app --reload
```

A API estará disponível em `http://localhost:8000`

## Endpoints

### 1. Obter Token (Login)
- **POST** `/token`
- Body (form-data):
  - username: user
  - password: 123

### 2. Ver Perfil do Usuário (Protegido)
- **GET** `/users/me`
- Header: `Authorization: Bearer <token>`

### 3. Ver Itens do Usuário (Protegido)
- **GET** `/users/me/items/`
- Header: `Authorization: Bearer <token>`

## Documentação

- Swagger UI: `http://localhost:8000/docs`
- ReDoc: `http://localhost:8000/redoc`

## Credenciais de Teste

- Usuário: user
- Senha: 123 
