# Desafio Back-end Jr. AutoSCORE

## Avisos antes de começar
- Crie um repositório publico no seu GitHub sem citar nada relacionado a AutoSCORE.
- Faça seus commits no seu repositório.
- Você poderá consultar o Google, Stackoverflow ou algum projeto particular na sua máquina.

### Sobre o ambiente da aplicação:
- A linguagem de programação escolhida é Java 8 ou superior;
- Deve ser usado o Framework Spring;
- Recomendamos o uso dos seguintes projetos do ecossistema Spring: Spring Boot, Spring Web, Spring Data JPA;
- Pode ser usado um dos seguintes bancos de dados: MySQL, PostgreSQL ou H2;

## Objetivo
Temos um cadastro de veículos onde precisaremos das seguintes informações: Proprietário, CPF Proprietário, Placa, Chassi, Marca, Modelo e Status do Licenciamento. CPF e Placa deverão ser únicos no sistema. Sendo assim, seu sistema deve permitir apenas um cadastro com o mesmo CPF ou Placa;

Para um cadastro de um novo veículo, precisaremos passar apenas as seguintes informações: Proprietário, CPF e Placa. 

### Payload
Faça uma proposta de payload, se preferir, temos um exemplo aqui:

POST: /veiculos

```json
{
    "proprietario" : "José da Silva",
    "cpf" : "203.397.390-53",
    "placa" : "ABC1234"
}
```

Antes de persistir os dados no banco de dados, deverá ser consultada uma API externa, onde obteremos os dados do veículo e se o mesmo está licenciado.
Use este endereço para consultar os dados do veículo passando a placa: 
GET (https://my.api.mockaroo.com/veiculos?key=55ad1cd0&placa=ABC1234)

Depois de persistido os dados o retorno deverá consolidar os dados enviados juntamente com os dados obtidos da API Externa.

Exemplo: 

```json
{   "id" : 1
    "proprietario" : "José da Silva",
    "cpf" : "203.397.390-53",
    "placa" : "ABC1234",
    "marca": "Chevrolet",
    "modelo": "Suburban 1500",
    "chassi": "5TDBKRFH2FS979708",
    "licenciado": true
}
```

# Avaliação
Serão avaliados a sintaxe, as escolhas de bibliotecas e a funcionalidade da aplicação.

## O que será um Diferencial
- Validação dos dados de entrada
- Código limpo e organizado (nomenclatura, etc)
- Modelagem de Dados
- Tratamento de erros
- Uso de Design Patterns

# Materiais úteis (Referencia)
- https://www.oracle.com/br/technical-resources/articles/dsl/crud-rest-sb2-hibernate.html
- https://vitormoschetti.medium.com/primeiro-crud-com-spring-boot-5b7abd118ded
- https://www.youtube.com/watch?v=biCJIlqA334
- https://www.linkedin.com/pulse/consumindo-apis-com-java-e-spring-boot-usando-um-guia-dhionson/
- https://github.com/marcosrebelo97/demo-rest-template

