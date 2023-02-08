# ApiNodeShop

[Clique aqui para ver o Front utilizado nesse projeto](https://github.com/yan-moura19/NodeShopFront)

* 1 - Guia de instalação do projeto
* 2 - Detalhamento das rotas e dos modelos
* 2.1 - Models
* 2.2 - Routers
* 2.3 - Index/Login
* 3 - Passo a Passo do projeto
* 4 - Requisitos do projeto
* 5 - Conclusão e avaliação do meu desempenho no projeto

Obs: o MongoDB pode não aceitar o IP da sua máquina

 

### E-commerce com Login, Tela de produtos, Tela de Carrinho.
### Tecnologias usadas: Node js, MongoDb e Flutter


## 1 - Instalar dependencias do projeto 
```
npm install
```

### Rodar aplicação
```
npm start
```

### 2.1  
#### User.js (Usuário)
```
{
    nome: String,
    usuario: String,
    senha: String
}
```
#### Compra.js (Compra/Pedido)
```
{
    usuario : String,
    produtos : String,
    valor: String
}
```

### 2.2
#### Post Compras (inserir uma compra) 

##### Arquivo CompraRouters.js
Rota = "/compra"

Verbo HTTP = POST

Body recebe um Json. 
Nenhum atributo pode ser nulo. (usuarios, produtos e valor)
```
{
    "usuario" : "YanTeste",
    "produtos": "['{Produto1}','{Produto2}','{Produto3}','{Produto4}']", 
    "valor": 150
}
```
Tipo de dados:
```
    "usuario" : String,
    "produtos": String de uma lista de objeto Json, 
    "valor": Number 
```

#### Get  Compras (inserir uma compra) 

Rota = "/compra" 

Verbo = GET

Retorna uma lista do objeto compra 
```
{
    "usuario" : "YanTeste",
    "produtos": "['{Produto1}','{Produto2}','{Produto3}','{Produto4}']", 
    "valor": 150
}

{
    "usuario" : "YanTeste2",
    "produtos": "['{Produto1}','{Produto2}','{Produto3}','{Produto4}']", 
    "valor": 259
}
```
### 2.3
#### Post Usuário (inserir um usuário) 
Rota = "/auth/register" 

Verbo = POST

Body recebe um Json. 
Nenhum atributo pode ser nulo. (usuarios, produtos e valor)
O método verifica:
* Se o usuário já existe  

```
{
    "nome": "Yan",
    "usuario": "Yan1234",
    "senha": "1234"
}
```
#### Post Login (efetuar Login) 
Rota = "/auth/login" 

Verbo = POST

Body recebe um Json. 
Nenhum atributo pode ser nulo. (usuarios, produtos e valor)
O método verifica:
* Se o usuário existe  
* Se a senha é correta  
```
{
   "usuario": "Yan123",
    "senha" : "123"
}
```

Retorna
```
{
   "usuario": "Yan123",
    "Token" : "kdalopof6+fa496f464dsf946+sda9"
}
```

### 3 - Passo a Passo do projeto (Tasks)
* Levantamento e análise dos Requisitos (Requisitos listados no 4º tópico)
* Definir  as tecnologias (Node Js e Flutter).
* Criar Back-end em Node Js.
* Criar aplicação Flutter.
* Criação da tela de Login.
* Criação da tela de Listar Produtos.
* Criação da tela de Carrinho.
* Efetuar Compra.
* Criação da tela de Produtos Filtrados.

### 4 - Requisitos do projeto

* Listar Produtos.(Essencial)
* Filtrar e pesquisar produtos.(Essencial)
* Carrinho de compras.(Importante)
* Registrar comprar.(Essencial)
* Criar usuario.("Extra")
* Efetuar Login.("Extra")

### 5 - Conclusão e avaliação do meu desempenho no projeto

* Enfrentei alguns problemas (De CORS), mas consegui resolver.
* Adcionei a tela de login para aumentar a "realidade" da aplicação.
* A validação de token não foi aplicada em nenhum método, foi apenas uma demonstração.
* Tive um bom resultado e tentei deixar a aplicação mais intuitiva possível e a documentação (README) mais objetiva e clara possivel.
* Adquiri novas experiências e aumentei a capacidade de resolução de problemas.
* Desenvolvi novas habilidades e conhecimento em Flutter e Node Js
* Fiz a aplicação em um curto espaço de tempo, geralmente no Fim de semana. Poderia ter refatorado mais e implemntado alguns detalhes. No entanto, cumpri com os requisitos. 
