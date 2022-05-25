<h1>Code Challenge - Backend Engineer - IZA.com.vc</h1>
Parabéns por ter passado de fase e ter chegado até aqui. Estamos empenhados em encontrar pessoas incríveis para fazer parte do nosso time de tecnologia e acreditamos que você tem as características que buscamos. 

Preparamos um desafio que consiste na criação de uma **API Rest** com Modelagem de dados, Autenticação, Relacionamento entre tabelas, Cadastro (Create), Listagem (Read), Atualização (PUT) e Deleção (Delete).

**Modelagem de dados**

Trabalhe na modelagem das tabelas do banco de dados antes de começar a codificar, ao finalizar, anexe uma imagem com a modelagem dos dados que você criou no [README.md](http://readme.md) do seu projeto.

- **Atente-se aos relacionamentos que devem existir entre as tabelas.**

Estrutura de Dados:

- Cliente → Nome, Email, Endereço (cep, estado, cidade, número) e senha.
- Produto → Nome, preço, descrição e foto (imagem)

Regras:

- Um cliente pode cadastrar apenas um endereço. (1x1)
- O endereço deve estar armazenado em uma tabela separada (não pode ficar na mesma tabela que os usuários).
- Um cliente pode cadastrar vários produtos. (1xN)

**Endpoints:**

/Signup →

- O cliente deve informar seus dados para realizar o cadastro, sendo que nome, email e senha são obrigatórios. **Nome, Email, Endereço (cep, estado, cidade, número) e senha.**

/Auth → 

- Email e senha são obrigatórios.
- Deve ser retornado um token JWT para autenticação quando os dados informados são validos.

/Users → ****

- Deve retornar todos os usuários cadastrados no endpoint de /Signup.
- A senha não pode aparecer na listagem.

/User/{id} → 

- Deve ser possível recuperar um cliente pelo id.
- Adicionar validação para id inexistente/inválido quando informado.
- Deve ser possível editar os dados de um usuário.

/Product → 

- Deve ser possível cadastrar um produto. Todos os campos são obrigatórios: Nome, preço, descrição e foto (imagem).
- O produto cadastrado deve ser associado ao usuário autenticado (JWT).
- Deve ser possível editar os dados do produto.

/Products → 

- Apenas usuários autenticados podem consultar esse endpoint (JWT).
- Listar todos os produtos cadastrados pelo usuário autenticado (JWT).

/Product/{id} → 

- Deve ser possível recuperar um produto pelo seu id.
- Adicionar validação para id inexistente/inválido quando informado.

/User/products/{userId} → 

- Deve ser possível recuperar todos os produtos de um cliente, pelo id do cliente.

**Requisitos:**

- Documente os endpoints com swagger ou nos envie os endpoints em uma collection do postman.
- Variáveis, funções e todo o código deve ser escrito em inglês.
- Utilize o ORM de sua preferência para fazer as consultas. Não utilize procedures ou queries puras.
- Conventional commits [https://www.conventionalcommits.org/en/v1.0.0/](https://www.conventionalcommits.org/en/v1.0.0/)
- O arquivo [README.md](http://readme.md) do projeto deve detalhar o que é a aplicação e como a mesma pode ser instalada e executada.
- Utilização correta de status codes (200, 201, 400, 500, 401, 404) - quando aplicável
- Utilização correta de REST API methods: [https://docs.oracle.com/en/cloud/saas/enterprise-performance-management-common/prest/rest_api_methods.html](https://docs.oracle.com/en/cloud/saas/enterprise-performance-management-common/prest/rest_api_methods.html)

**Desejável, porém não obrigatório:**

- Docker
- Arquitetura limpa

**Ao finalizar**

Envie o teste para um repositório do **Github** e nos envie o link. Ou adicione o usuário @felipebenevides se for um repositório privado.

Boa sorte!
