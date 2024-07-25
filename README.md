# Publicando Sua API REST na Nuvem Usando Spring Boot 3, Java 17 e Railway
### Santander 2024 - Backend com Java. Java RESTful API criada para a Santander Dev Week - Data de início 23/07/2024 e data limite de encerramento 29/07/2024
### Desenvolvimento Java com IA - Data de início 23/07/2024 e data limite de encerramento 19/08/2024
## Diagrama de classe

```mermaid
classDiagram
  class User {
    - String name
    - Account account
    - List<Feature> features
    - Card card
    - List<News> news
  }
  class Account {
    - String number
    - String agency
    - float balance
    - float limit
  }
  class Feature {
    - String icon
    - String description
  }
  class Card {
    - String number
    - float limit
  }
  class News {
    - String icon
    - String description
  }

  User "1" *-- "1" Account
  User "1" *-- "N" Feature 
  User "1" *-- "1" Card 
  User "1" *-- "N" News 

```
## Principais Tecnologias

- Java 21: Foi utilizado a versão LTS mais recente do Java para tirar vantagem das últimas inovações que essa linguagem robusta e amplamente utilizada oferece;
- Spring Boot 3: Sendo a nova versão do Spring Boot, que maximiza a produtividade do desenvolvedor por meio de sua poderosa premissa de autoconfiguração;
- Spring Data JPA: Exploraremos como essa ferramenta pode simplificar nossa camada de acesso aos dados, facilitando a integração com bancos de dados SQL;
- OpenAPI (Swagger): Na documentação da API foi usando a OpenAPI (Swagger), perfeitamente alinhada com a alta produtividade que o Spring Boot oferece;
- H2 Database: Banco de dados SQL em memória, sendo uma ótima opção para testes.


## Json para o método Post no OpenAPI
```
{
	"name": "David",
	"account":{
		"number": "00000000-0",	
		"agency": "0000",
		"balance": 1324.64,
		"limit": 1000.00
	},
	"features":[
	 {
		"icon": "URL",
		"description": "Descrição da Feature"
	 }
	],
	"card":{
	 "number": "xxxx xxxx xxxx 0000",
	 "limit": 1000.00
	},
	"news":[
	 {
		"icon": "URL",				
		"description": "Descrição da novidade"
	 }
	]
}
```
