## Modelo de domínio

![GameList](https://github.com/user-attachments/assets/51a0ba03-04f9-4e7b-8319-06f163bd9f08)

## Apresentação (Resumo)

Projeto *Game List Manager*, gerência listas de jogos. Aqui, você pode organizar os jogos em listas personalizadas, adicionando informações como título, gênero, ano de lançamento, plataforma, pontuação, descrições. 

## Observações 

- Organização de jogos em listas personalizadas com posições específicas.

- O relacionamento entre jogos e listas é gerenciado por uma tabela intermediária chamada Belonging, onde tive que criar uma classe BelongingPK que encapsula os dois IDs, atributos que juntos formam a chave primária da entidade Belonging:

  - gameId (o ID do jogo)
  - listId (o ID da lista)

## Tecnologias utilizadas

- Java (Spring Boot)
- JPA
- Banco de dados PostgreSQL (Docker)
- APIs RESTful para criar, consultar e atualizar jogos e listas
- Processo de deploy com CI/CD
- Postman
- Arquitetura limpa com separação em camadas bem definidas:
  - Controller: Exposição das APIs REST.
  - Service: Implementação da lógica de negócios.
  - Repository: Comunicação com o banco de dados.
  - DTOs: Transferência de dados otimizada, evitando exposição direta das entidades.

## Como funciona o projeto?

#### Jogos: 

Cada jogo pode conter as seguintes informações:

- Título
- Gênero
- Ano de lançamento
- Plataforma(s)
- Pontuação
- Descrição detalhada
- Imagem ilustrativa

#### Listas de Jogos

- Crie listas personalizadas para organizar seus jogos.
- Relacione jogos às listas e defina suas posições específicas dentro delas.

## Como Executar?

#### Clonar o repositório:

```git clone https://github.com/seu-repositorio/game-list-manager.git```

#### Configurar o ambiente:

Certifique-se de ter Docker e PostgreSQL instalados.

Configure o arquivo application.properties com as credenciais do banco de dados.

#### Executar o projeto:

Com o Spring Boot:

```./mvnw spring-boot:run```
