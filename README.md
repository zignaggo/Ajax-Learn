# Ajax-Learn

## Utilização do AJAX

* Trazer as informações do back-end por meio de javascript ( Intermediário entre Back e Front )

* A.J.A.X - Asynchronous Javascript XML
---

## Status de requisição 

* [Status DOG Learn]('httpstatusdogs.com')

#### **Status mais comuns**

* 404 - NotFound
> Conteúdo não encontrado

* 200 - OK
> Conteúdo acessado com sucesso


## API FAKE PARA ESTUDO
* [API FAKE](reqres.in)


## Fetch API

* Enviar informações por meio do FETCH
* Primeiro parâmetro: URL
* Segundo parãmetro: HEADER (caso queira enviar informações)
> Para enviar temos que converter o objeto para string, por meio do stringify
```javascript
fetch('https://reqres.in/api/users' , {
            method: 'POST',
            body: JSON.stringify(dados)
        })
```
> Header com as informações do método, corpo, etc...

---

### **Feedback** 
Ao enviar algo para o servidor devemos informar o usuário se foi bem sucedido ou não, e fazemos isso por meio do **then**.

```javascript
fetch('https://reqres.in/api/users' , {
    method: 'POST',
    body: JSON.stringify(dados)
    headers: {
        "Content-type" : "application/json"
    }
}).then( (response) => {
    console.log(response)
})
```
---
### **Método GET**

Receber informações do servidor
```javascript
fetch('https://reqres.in/api/users')
    .then( (response) => response.json())
    .then( (response) => console.log(response) )
```
---
### **Tratamento de erros**

Tratar erros que podem ocorrer ao fazer a requisição
```javascript
fetch('https://reqres.in/api/users')
    .then( (response) => response.json())
    .then( (response) => console.log(response) )
    .catch( (err) => {
        console.log('deu erro tá: ', err )
    })
```
#### Executar vários Requests
```javascript
    const getManyRequests = async () => {
        const [requestOne, requestTwo] = await Promisse.all([
            fetch('url'),
            fetch('url2')
        ])

        const dataRequestOne = await requestOne.json()
        const dataRequestTwo = await requestTwo.json()

    }
```



## Protocolo HTTP  

* Protocolo de transferência de HIPERTEXTO
* Usado para comunicação: Cliente e Servidor
* Dividido em Request e Response
* Stateless - Sem estado, ou seja, toda conexão é como se fosse uma nova conexão

#### Métodos das requisições
 
1. GET
    > Solicitar informações ao servidor, Parâmetros na url
1. POST
    > Salvar informação no servidor ( enviar ), Parâmetros no Corpo da requisição
1. PUT
    > Alterar informações no servidor
1. DELETE
    > Apagar informações no servidor
1. TRACE
    > Retorna o que o servidor recebeu, o request completo. Serve para o 
1. OPTIONS
    > Recebe informações do servidor se é possível realizar alguma ação, por exemplo, se consegue realizar um delete, o servidor retorna true 
1. CONNECT
    > o cara não falou, desgraçado...
1. HEAD
    > Retorna apenas o cabeçário
1. PATCH
    > Alterar informações no servidor:  pequenas alterações, por exemplo um campo apenas
#### Status Code
---
#### **Grupos de status**
*   1xx - Informação
*   2xx - Sucesso
*   3xx - Redirecionamento
*   4xx - Erro no Cliente
*   5xx - Erro no Servidor
---

#### Status mais Comuns
* 200 - OK
    > Requesição bem sucedida
* 201 - Created
* 404 - Not Found 
    > Recurso com o servidor não encontrada
* 403 - Forbidde
    > Cliente não tem acesso
* 401 - Unauthorized 
    > Não tem autenticação válida para fazer a requisição
* 500 - Internal Server Error 
    > Cagada no servidor

#### Parâmetros da Requisição

* Divisão de parâmetros e URL - **?**

    > https://www.google.com/search?q=teste

* Adicionar pararâmetros - **&**

    > https://www.google.com/search?q=teste&oq=teste&aqs=chrome

---

## Cabeçalhos de entidade

* Content-type
> Tipo do conteúdo: text/html ( padrão )

* Content-Length
> Tamanho do conteúdo: 50

---
### Links Vídeos

[Protocolo HTTP em detalhes #2 - Teoria (Super fácil)](https://www.youtube.com/watch?v=d_5iZJ8p9x8)