# Sobre os Arquivos e suas Funcionalidades:

> A base do TypeScript é o SoC: Separation of Concerns (Separação de preocupações), ou seja, cada arquivo deve ter uma única preocupação!

### Models =>

Representação de como um dado é salvo na aplicação.

- É responsável pelo formato dos dados.

### Repositories =>

Trabalhar com o dado.

- Uma conexão entre a persistência dos dados "banco de dados" e a rota;
- Dentro dele, buscamos as informações no BD, teremos o CRUD "método find, create";
- Apenas o repositório deve ter acesso aos dados da entidade, se quiser buscar, criar, deletar ou atualizar, basta criar métodos públicos dentro do repositório e usar esses métodos onde precisar;
- É necessário instanciar o repositório quando for utiliza-lo.

### Services =>

Armazenar a regra de negócio da aplicação.

- Cria um arquivo por responsabilidade, uma criar, outro para atualizar...

> Sempre que o service tiver uma dependência externa, ao invés de instânciar uma nova classe dentro do service, usamos a Dependency Inversion (SOLID), para receber essa classe como uma parâmetro. Isso garante que a aplicação inteira esteja usando o mesmo repositório.

### DTO - Data Transfer Object =>

- Sempre que for transmitir dados de um arquivo para outro, além de usar o DTO, o formato deve ser objeto;
- Em outras palavras, o DTO funciona como uma interface, dizendo ao método quais dados ele recebe e qual exatamente está faltando.

> Tips: Pode-se usar a tecla Ctrl ao por o mouse em cima da utilização da interface, assim o VsCode vai mostrar exatamente todas as variáveis e seus respectivos tipos.
> Quando recebemos os dados do service, é comum nomear a interface como `Request`.
