<!-- PROJECT LOGO -->
<br />
<p align="center">
  <h2 align="center">Desafio Omni Channel</h2>

  <p align="center">
    Serviço HTTP resolvendo a funcionalidade de Omni Channel para um e-commerce
    <br />
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Tabela de conteúdos</summary>
  <ol>
    <li>
      <a href="#sobre-o-projeto">Sobre o Projeto</a>
      <ul>
        <li><a href="#tecnologias-utilizadas">Tecnologias utilizadas</a></li>
      </ul>
    </li>
    <ul>
        <li><a href="#regras-de-negócio">Regras de negócio</a></li>
      </ul>
    </li>
    <li>
      <a href="#instruções-gerais">Instruções gerais</a>
      <ul>
        <li><a href="#instalação">Instalação</a></li>
      </ul>
    </li>
    <ul>
        <li><a href="#configurando">Configuração</a></li>
      </ul>
    </li>
    <li><a href="#utilizando-a-api">Utilizando a API</a></li>
      <ul>
        <li><a href="#endpoints">Endpoints</a></li>
      </ul>
        <ul>
        <li><a href="#swagger">Swagger</a></li>
      </ul>
    </li>
    </li>  
    <li><a href="#equipe">Equipe</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## Sobre o projeto

Esse projeto tem como objetivo o desenvolvimento de um serviço HTTP que resolve a funcionalidade de um Omni Channel do Cliente, ou seja, adicionar ou remover produtos do carrinho de compras, bem como consultar a lista dos produtos disponíveis e seu histórico de compras.

### Tecnologias Utilizadas

O projeto foi criado usando as tecnologias:
* [JavaScript]
* [Node.Js]
* [PostgreSQL]
* [Swagger]

### Regras de Negócio

* Cada cliente deve ter um e-mail cadastrado;
* O cliente pode adicionar ou remover produtos de seu carrinho e finalizar a compra;
* O cliente só poderá comprar UM produto por <i>tipo</i>;
* Ao final da compra o status se altera de <i>carrinho</i> para <i>realizada</i> e uma <i>loja</i> é associada ao <i>pedido</i>;
* A loja onde a compra foi retirada deve atualizar o status de <i>realizada</i> para <i>retirada</i>;
* O cliente pode consultar todos os produtos e lojas disponíveis, o carrinho atualizado e o histórico de pedidos;
* Somente o adminstrador tem acesso à lista de clientes.

<!-- GETTING STARTED -->
## Instruções Gerais

A seguir estão as instruções para a instalação, configuração e uso da API do projeto.

### Instalando

1. Clonar o repositório
```sh
   git clone https://github.com/ANNEBORTOLI/luizaCode-projetoFinal.git
```

2. Instalando os pacotes 
```sh
    npm install
```  
3. Rodar migrations
```sh
    npm run migrate
```  
-OU-

```sh
    npx sequelize db:migrate
```  
4. Rodar seeders
```sh
    npm run seed
```  
-OU-
```sh
    npx sequelize db:seed:all
```  
5. Executar a API localmente
```sh
    npm run dev
```  

### Configurando

1. Alterar a configuração dos bancos de dados na pasta [ :open_file_folder:luizaCode-projetoFinal\src\database\config\database.js ].
Trocar a senha em <i>password</i> e o nome do banco em <i>database</i>.


![Configuração do banco][config-bd]

2. Em caso de conflito de porta, alterar em [ :open_file_folder: luizaCode-projetoFinal\bin\www ] na linha 15:
```
var port = normalizePort(process.env.PORT || '3000') //3000 para uma de sua escolha
```

<!-- USAGE EXAMPLES -->
## Utilizando a API

### Endpoints

O usuário tem acesso aos seguintes endpoints:
- Cadastro
- Login
- Produtos
- Lojas

![Endpoints Clientes][endpoints-cliente]

Todos podem acessar a lista de produtos e lojas:

![Endpoints globais][endpoints-globais]

Apenas o adminstrador tem acesso aos endpoints:
- Retirada de produtos
- Lista de clientes

![Endpoints Administrador][endpoints-admin]


### Rodando aplicação com Swagger

No navegador, digitar <a href="localhost:3000/docs">localhost:3000/docs</a>. Se necessário, trocar 3000 pela porta configurada. 

<!-- CONTACT -->
## Equipe

- [Anne Bortoli](https://github.com/ANNEBORTOLI)
- [Gabriela Tavares](https://github.com/GabiTavaresV)
- [Jaqueline Vieira Abreu](https://github.com/jaquelineabreu)
- [Mariana Aguiar](https://github.com/marianadesouzaaguiar)
- [Rafaela Nakashima](https://github.com/rafanak)



<!-- MARKDOWN LINKS & IMAGES -->
[config-bd]: images/config-bd.png
[endpoints-cliente]: images/ep-cliente.png
[endpoints-globais]: images/ep-global.png
[endpoints-admin]: images/ep-admin.png

