# Sistema de Gestão de Vendas Online

## Informações do Aluno

- **Nome**: Jose Almir Mariano Figueiredo Junior
- **Projeto**: Sistema de Gestão de Vendas Online
- **Instituição**: UNICAP
- **Curso**: Ciência da Computação
- **Disciplina**: Banco de Dados I
- **Professor**: Lucas Rodolfo Celestino de Farias

## Descrição do Projeto

Este projeto tem como objetivo por em prática os conhecimentos ensinados em sala sobre Diagrama Entidade-Relacional(ER). Para atingir esse propósito, foi pensado e construído um Diagrama ER de gestão de vendas online, que aborda desde o cadatro de clientes até a entrega do produto.

### Requisitos Mínimos Implementados

#### Entidades Principais:
- Foram representadas as entidades essenciais para o sistema:  Cliente, Produto, Pedido e Pagamento.

#### Atributos Essenciais:
- Todas as entidades foram estruturadas com atributos essenciais. Por exemplo: Cliente inclui nome e contato; Produto inclui descrição e valor; Pedido registra a data e o valor total; Pagamento especifica o método de pagamento e o status.

#### Relacionamentos:
- Os relacionamentos entre entidades foram estabelecidos, de modo que, inclui a relação de um Pedido contendo vários Produtos, e um Cliente realizando vários Pedidos.

#### Cardinalidade:
- Foram utilizadas cardinalidades para representar a quantidade de entidades envolvidas em cada lado dos relacionamentos, como a relação (1,N) no lado do Cliente, na relação Cliente e Pedido.

#### Agregações:
- As agregações foram implementadas para estabelecer conceitos complexos, como um Pedido contendo vários produtos.


### Requisitos Adicionais e Motivações:

#### Entidade Envio/Entrega:
- **Motivação**: Aumentar a precisão no rastreamento e na gestão de logística da entregas da empresa.

#### Entidade Estoque:
- **Motivação**: Melhorar o controle de produtos e garantir a disponibilidade.

#### Entidade Fornecedor:
- **Motivação**: Melhorar o controle sobre os fornecedores de produtos, com o objetivo de facilitar e gerenciar o fornecimento de produtos.

#### Entidade Funcionário (Entregador, Analista de Compras, Estoquista, Empacotador):
- **Motivação** Gerenciar os funcionários por função, com o objetivo de entender as relações e atributos de cada cargo na empresa.

