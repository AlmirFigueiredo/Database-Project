# Sistema de Gestão de Vendas Online

## Informações do Aluno

- **Nome**: Jose Almir Mariano Figueiredo Junior
- **Projeto**: Sistema de Gestão de Vendas Online
- **Instituição**: UNICAP
- **Curso**: Ciência da Computação
- **Disciplina**: Banco de Dados I
- **Professor**: Lucas Rodolfo Celestino de Farias

## Descrição do Projeto

Este projeto tem como objetivo por em prática os conhecimentos ensinados em sala sobre Diagrama Entidade-Relacional(ER). Para atingir esse propósito, foi pensado e construído um Diagrama ER de gestão de vendas online, que aborda desde o cadastro de clientes até a entrega do produto.

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

## Visão Geral dos Atributos das Entidades do Diagrama
### Cliente
- `cliente_id`: Identificador único para cada cliente.
- `primeiro_nome`: Primeiro nome do cliente.
- `sobrenome`: Sobrenome do cliente.
- `email`: Endereço de email para contato com o cliente.
- `senha`: Senha de acesso do cliente.
- `genero`: Gênero do cliente.
- `end`: Endereço do cliente.
- `telefone`: Número de telefone do cliente.
- `data_nascimento`: Data de nascimento do cliente.

### Pedido
- `pedido_id`: Identificador único de cada pedido.
- `cliente_id`: Indica o cliente que fez o pedido.
- `data_pedido`: Data em que o pedido foi efetuado.
- `valor_total`: Valor total do pedido (soma de todos os produtos e quantidades).
- `status_pedido`: Situação atual do pedido (por exemplo, "pendente" ou "entregue").

### Produto
- `produto_id`: Identificador único de cada produto.
- `nome`: Nome comercial do produto.
- `descricao`: Descrição detalhada do produto.
- `catego_prod`: Categoria à qual o produto pertence.
- `valor`: Preço unitário do produto.

### Estoque
- `estoque_id`: Identificador único do estoque.
- `produto_id`: Identificador do produto no estoque.
- `setor`: Localização específica do produto no estoque.
- `qtd_disponivel`: Quantidade disponível do produto em estoque.
- `qtd_minima`: Quantidade mínima definida em estoque para o produto.
- `data_ult_att`: Data da última atualização do estoque.

### Pagamento
- `pagamento_id`: Identificador único para cada pagamento.
- `valor_pago`: Quantia paga.
- `status_pagamento`: Status do pagamento (por exemplo, "concluído" ou "pendente").
- `pedido_id`: Indica o pedido ao qual o pagamento se refere.
- `metodo_pag`: Método utilizado para o pagamento.
- `data_pagamento`: Data em que o pagamento foi realizado.

### Envio/Entrega
- `entrega_id`: Identificador único da entrega.
- `pedido_id`: Indica o pedido à ser entregue/entregado.
- `codigo_rast`: Código utilizado para rastrear o envio.
- `status_entrega`: Status atual da entrega (por exemplo, "Entregue").
- `data_postagem`: Data de envio do produto.
- `data_prev_entrega`: Data estimada para a chegada do produto no endereço do cliente.

### Fornecedor
- `fornecedor_id`: Identificador único do fornecedor.
- `nome_fantasia`: Nome comercial do fornecedor.
- `end`: Endereço comercial do fornecedor.
- `contato`: Informações de contato do fornecedor.
- `prod_fornecidos`: Produtos que são fornecidos por esse fornecedor.

### Entregador
- `modelo_veiculo`: Modelo do veículo utilizado para entregas.
- `placa_veiculo`: Placa de registro do veículo.
- `cnh`: Número da Carteira Nacional de Habilitação do entregador.

### Funcionário
- `primeiro_nome`: Primeiro nome do funcionário.
- `sobrenome`: Sobrenome do funcionário.
- `telefone`: Número de telefone do funcionário
- `carga_horaria`: Carga horária semanal do funcionário.
- `funcionario_id`: Identificador único para cada funcionário.
- `salario`: Salário mensal do funcionário.
- `email`: Endereço de email para contato com funcionário.

## Visão Geral dos Relacionamentos do Diagrama

### Cliente e Pedido
- **Realiza**: Cada cliente pode realizar vários pedidos, mas cada pedido é realizado por um único cliente.
  - Cardinalidade: (1,N) para Cliente e (1,1) para Pedido.

### Pedido e Produto
- **Contém**: Um pedido pode conter um ou vários produtos, e um produto pode estar em um ou vários pedidos.
  - Cardinalidade: (1,N) para Pedido e (1,N) para Produto.d

### Produto e Estoque
- **Está em**: Um ou mais produtos podem estar no estoque, porém um estoque pode conter vários produtos. 
  - Cardinalidade: (1,N) para Produto e (1,1) para Estoque.

### Cliente e Pagamento
- **Gera**: Cada cliente pode gerar vários pagamentos, e cada pagamento é associado a um pedido de um cliente.
  - Cardinalidade: (1,N) para Cliente e (1,1) para Pagamento.

### Cliente e Produto
- **Avalia**: Cada cliente avalia um produto e um produto pode ser avaliado por varios clientes.
  - Cardinalidade: (1,N) para Cliente e (1,1) para Produto. 

### Pedido e Envio/Entrega
- **Contém**: Um envio possui um pedido e um pedido é enviado por um envio.
  - Cardinalidade: (1,1) para Pedido e (1,1) para Envio/Entrega.

### Fornecedor e Produto
- **Fornece**: Fornecedores podem fornecer vários produtos, e um produto pode ser fornecido por vários fornecedores.
  - Cardinalidade: (1,N) para Produto e (1,N) para Fornecedor.

### Empacotador e Pedido
- **Prepara**: Cada empacotador pode preparar vários pedidos, porém um pedido so pode ser prerado por um empacotador.
  - Cardinalidade: (1,N) para Empacotador e (1,1) para Pedido.

### Analista de Compras e Fornecedor
- **Compra do**: Um ou mais analistas de compra podem comprar de um ou mais fornecedores.
  - Cardinalidade: (1,N) para Analista de Compras e (1,N) para Fornecedor. 

### Entregador e Entrega/Envio
- **Realiza**: Um ou mais entregadores entrega/entregam um ou mais pedidos.
  - Cardinalidade: (1,N) para Entregador e (1,N) para Entrega/Envio. 

### Funcionario (Auto-relacionamento)
- **Supervisiona**: Um funcionário pode ser supervisor de outro funcionário, assim como pode ser supervisionado por outro funcionário.
  - Cardinalidade: (0,1) para o supervisor e (0,N) para o supervisionado.