# Sobre os arquivos:

### Repositories =>

- Uma conexão entre a persistência dos dados "banco de dados" e a rota;
- Dentro dele, buscamos as informações no BD, teremos o CRUD "método find, create";
- Apenas o repositório deve ter acesso aos dados da entidade, se quiser buscar, criar, deletar ou atualizar, basta criar métodos públicos dentro do repositório e usar esses métodos onde precisar;
- É necessário instanciar o repositório quando for utiliza-lo.

### Models =>

- É responsável pelo formato dos dados.
