# Workshop Java - MongoDB

Este projeto foi desenvolvido como parte de um workshop sobre Java com MongoDB. Aqui estão os principais componentes e detalhes do projeto:

Este projeto foi desenvolvido por Danilo Garcia Paravani.

## Tecnologias Utilizadas
- Java
- Spring Boot
- MongoDB
- Maven
- Postman

## Como Rodar o Projeto
1. Clone o repositório para sua máquina local:
   ```bash
   git clone https://github.com/DaniloParavani/workshop-spring-boot-mongodb.git
   ```


1. No terminal, navegue até o diretório do projeto.


2. Certifique-se de ter o Maven instalado. Execute o seguinte comando para compilar e construir o projeto:
   ```bash
   mvn clean install
   ```


3. Após a construção, você pode executar o aplicativo Spring Boot usando o seguinte comando:
   ```bash
   mvn spring-boot:run
    ```
   A aplicação estará acessível em http://localhost:8090


4. A aplicação utiliza o MongoDB como banco de dados. A configuração pode ser encontrada no arquivo application.properties:
  ```bash
  server.port = ${port:8090}
  spring.data.mongodb.uri=mongodb://localhost:27017/workshop_mongo
  ```

   
## Endpoints da API

### Usuários

- GET /users: Retorna a lista de todos os usuários.
- GET /users/{id}: Retorna os detalhes de um usuário específico.
- POST /users: Cria um novo usuário.
- DELETE /users/{id}: Exclui um usuário.
- PUT /users/{id}: Atualiza os dados de um usuário existente.
- GET /users/{id}/posts: Retorna a lista de posts associados a um usuário específico.

  #### Exemplo de body para os métodos POST e PUT
  
  ![image](https://github.com/DaniloParavani/workshop-spring-boot-mongodb/assets/87047957/472c3d4e-c545-4d6a-bc71-570405c0aecc)


### Post

- GET /posts/{id}: Retorna os detalhes de um post específico.
- GET /posts/titlesearch?text={text}: Retorna posts que contenham o texto pesquisado no título.
- GET /posts/fullsearch?text={text}&minDate={minDate}&maxDate={maxDate}: Retorna posts de acordo com os parâmetros de pesquisa.
