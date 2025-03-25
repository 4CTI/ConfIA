# Documentação da API - 4Cia

Esta documentação detalha os endpoints da API relacionados as consultas do LocalizAI..

---

### **URL de requisição:** `https://api.4ciweb.com`

---



## Endpoint de Login

### **POST** `/api/Login`

**Descrição:** Efetua login na API para obter o token necessário para autenticação.

### Exemplo de Requisição

```json
{
  "Username": "NomeDeUsuario",
  "Password": "Senha"
}
```

### Parâmetros

- **Sem parâmetros de URL**

### Corpo da Requisição

Formato `application/json`:

```json
{
  "username": "string",
  "password": "string"
}
```





## Endpoint do ConfIA

### **GET** `/api/ScoreCalculator/{cpfCnpj}`

**Descrição:** Calcula o score de um CPF ou CNPJ.

---

## **URL**

`https://api.4ciweb.com/api/ScoreCalculator/{cpfCnpj}`

---

## **Método**

`GET`

---

## **Headers**

- `accept`: `*/*`
- `Authorization`: `Bearer <seu_token>`

---

## **Path Parameters**

| Campo     | Tipo     | Obrigatório | Descrição                      |
|-----------|----------|-------------|--------------------------------|
| `cpfCnpj` | `string` | Sim         | CPF ou CNPJ a ser consultado. |

---

## **Exemplo de Requisição (curl)**

```bash
curl -X 'GET' \
  'https://api.4ciweb.com/api/ScoreCalculator/CPFouCNPJ' \
  -H 'accept: */*' \
  -H 'Authorization: Bearer <seu_token>'


### Respostas

- **200**: Solicitação bem-sucedida.
- **400**: Ocorreu uma falha durante a solicitação.
- **401**: Não autorizado (token ausente ou inválido).
- **403** - Acesso proibido.

---
