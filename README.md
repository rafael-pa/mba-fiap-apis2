# mba-fiap-apis
Projeto final para a disciplina de desenvolvimento de Microsserviços e APIs

## Parte 2 - Cadastro de Informações Financeiras
### Para acesso a estes endpoints é necessário o token gerado no login da [api usuarios](https://github.com/rafael-pa/mba-fiap-apis) no header da requisição ("token")


### /api/financeiro (GET)
- Retorno: lista de informações financeiras cadastradas
```json
{
    "output": "ok",
    "payload": [
        {
            "_id": "6365a6c0d7faaf8ea7394b59",
            "nome_titular": "Teste do Testador",
            "nome_banco": "Banco do Teste",
            "tipo_conta": "Corrente",
            "limite_cartao": 999.99,
            "__v": 0
        }
    ]
}
```

### /api/financeiro/cadastro (POST)
- Entrada: dados financeiros (todos são obrigatórios)
```json
{
    "nome_titular": "Teste do Testador",
    "nome_banco": "Banco do Teste",
    "tipo_conta": "Corrente",
    "limite_cartao": 999.99
}
```
- Retorno: dados financeiros
```json
{
    "output": "ok",
    "payload": [
        {
            "_id": "6365a6c0d7faaf8ea7394b59",
            "nome_titular": "Teste do Testador",
            "nome_banco": "Banco do Teste",
            "tipo_conta": "Corrente",
            "limite_cartao": 999.99,
            "__v": 0
        }
    ]
}
```

### /api/financeiro/atualizar/:id (PUT)
- Entrada: dados a serem atualizados 
```json
{
    "tipo_conta": "Poupança"
}
```
- Retorno:
```json
{
    "output": "Senha atualizada!",
    "payload": {
        "_id": "63659e74a394c4870f8a19e9",
        "nome_titular": "Rafael Andrade",
        "nome_banco": "Banco do Brasil",
        "tipo_conta": "Poupança",
        "limite_cartao": 1532.49,
        "__v": 0
    }
}
```

### /api/financeiro/apagar/:id (PUT)
#### Sem dados de entrada e saída

-------------
