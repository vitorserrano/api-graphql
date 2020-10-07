<h4 align="center"> 
  <img src=".github/graphql-node-mongo.png" width="500px">

API com <a href="https://graphql.org/">GraphQL</a> + <a href="https://nodejs.org/en/">Node</a> + <a href="https://www.mongodb.com/">MongoDB</a>

</h4>

## Conteúdo

- [O que é GraphQL](#-o-que-é-graphql)
- [Porque utilizar](#-porque-utilizar-graphql)
- [Construindo sua primeira API GraphQL](#-construindo-sua-primeira-api-graphql)

  - [API](#-api)

    - [Entendendo o GraphQL](#-entendendo-o-graphql)

    - [Pacotes e dependências](#-pacotes-e-dependencias)

    - [Estrutura de pastas](#-estrutura-de-pastas)

  - [Banco de dados](#-banco-de-dados) -[Docker](#-docker)

## O que é GraphQL?

[GraphQL](https://graphql.org/) é uma linguagem de consulta e ambiente de execução voltado a servidores para as APIs, cuja prioridade é fornecer exatamente os dados que os clientes solicitam e nada mais.

## Porque utilizar GraphQL?

- As chamadas do GraphQL são processadas em uma única transmissão com ida e volta. Os clientes recebem exatamente o que solicitam, sem mais dados do que o necessário (overfetching).

- Os tipos de dados são bem definidos, o que reduz as falhas de comunicação entre o cliente e o servidor.

- O GraphQL permite evoluir a API de uma aplicação sem prejudicar as consultas existentes.

## Construindo sua primeira API GraphQL

Antes de começarmos a codar, precisamos ter em mente alguns conceitos do GraphQL que irão nos ajudar.

<a id="entendendo-o-graphql"></a>

<details><summary>Entendendo o GraphQL</summary>
<p>

Abaixo estão listados alguns dos conceitos mais importates para trabalhar com GraphQL

- Qualquer request GraphQL é do tipo **POST**

- Toda request bate no mesmo endpoint **(/graphql)**

- Query -> Obter informações, em comparativo ao REST seria o método HTPP **(GET)**

- Mutation -> Manipular dados, novamente em comparativo ao REST seria o equivalente aos métodos HTTP **(POST/PUT/PATCH/DELETE)**

- Subscription -> Real Time/WebSockets

- Scalar Types -> String, Int, Boolean, Float e ID

</p>
</details>

<a id="pacotes-e-dependencias"></a>

<details><summary>Pacotes e dependências</summary>
<p>

Para criar nossa API, precisamos instalar alguns pacotes para facilitar a nossa vida.

- Inicialização do arquivo `package.json`

  - `yarn init -y`

- Utilização do ES6 no Node.js

  - `yarn add @babel/core @babel/cli @babel/preset-env @babel/node -D`

- Nodemoon

  - `yarn add nodemoon -D`
  - Dentro do arquivo `package.json` adicionar:
    ```json
        "scripts": {
          "dev": "npx nodemon --exec babel-node src/index.js -e js,gql"
        },
    ```

- GraphQL

  - `yarn add graphql`

- Mongoose

  - `yarn add apollo-server`

- Merge GraphQL Schemas
  - `yarn add merge-graphql-schemas`

</p>
</details>
