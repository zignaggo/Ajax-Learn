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
### **Feedback** 
Ao enviar algo para o servidor devemos informar o usuário se foi bem sucedido ou não, e fazemos isso por meio do **then**.

```javascript
fetch('https://reqres.in/api/users' , {
    method: 'POST',
    body: JSON.stringify(dados)
}).then( (response) => {
    console.log(response)
})
```
