# Projeto DSList

### Aprendizado:

• Conceitos
• Sistemas web e recursos
• Cliente/servidor, HTTP, JSON
• Padrão Rest para API web
• Estruturação de projeto Spring Rest
• Entidades e ORM
• Database seeding
• Padrão DTO

## 1º(s) passos 

• baixar os aqruivos no <a href="https://start.spring.io/;">Spring Initializr</a> com as seguintes configurações

<img src="https://raw.githubusercontent.com/vivianezzt/ds-list/main/img/projeto.png">

• No arquivo "pom.xml" do projeto já criado e importado para o SpringTools adicionar o plugin do maven abaixo:
````
<plugin>
	<groupId>org.apache.maven.plugins</groupId>
	<artifactId>maven-resources-plugin</artifactId>
	<version>3.1.0</version> <!--$NO-MVN-MAN-VER$ -->
</plugin>
````
• Na pasta "src/main/resources/application.properties" adicionar:

```
spring.profiles.active=${APP_PROFILE:test}
spring.jpa.open-in-view=false

cors.origins=${CORS_ORIGINS:http://localhost:5173,http://localhost:3000}

````

• Criar um arquivo "application-test.properties" e adicionar as configurações do banco de dados H2 com o seguinte código:


### H2 Connection
```
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.username=sa
spring.datasource.password=

# H2 Client
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

# Show SQL
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true

```


# Aula 02 - Relacionamentos

## Modelo de Domínio

<img src="https://raw.githubusercontent.com/vivianezzt/ds-list/main/img/dslist-model.png">

## Nesta fase do projeto vamos:

• Implementar modelo de domínio

• Atualizar seed da base de dados

• GameDTO, busca game por id

• Busca totas listas em /lists

• Consultar SQL, projection, busca de games por lista

• Relacionamentos N-N

• Classe de associação, embedded id

• Consultas SQL no Spring Data JPA

• Projection


# Preparação do ambiente

Preparação do ambiente
Docker ou Postgresql + pgAdmin ou DBeaver

Homologação local

1. Criar perfis de projeto * system.properties (DEV - PROD)
. Perfil de desenvolvimento e testes:
- test
- Banco de dados H2
. Perfil de homologação / staging:
- dev
- Banco de dados Postgres de homologação
. Perfil de produção:
- prod
- Banco
  
2. Gerar script da base de dados
* apagar arquivo gerado
  
3. Criar base de dados de homologação
   
4. Rodar app no modo dev e valida
   

## Aprendizado:

• Perfis de projeto

• Ambiente local com Docker Compose

• Processo de homologação local

• Processo de deploy com CI/CD

• Configuração de CORS

### Créditos &copy; <a href="https://devsuperior.com.br/bootcamp">Dev superior</a>
### Prof.<a href="https://www.youtube.com/@DevSuperior"> Nélio Alves</a> na semana Intensivão Java Spring - DevSuperior - Nélio Alves (2023) | de 10/07/23 à 14/07/23





