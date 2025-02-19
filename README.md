# Projeto de Modelagem de Banco de Dados para Ecommerce

Este projeto tem como objetivo modelar um banco de dados para um ecommerce, abrangendo clientes (pessoas físicas e jurídicas), pagamentos e entregas.

## Tabelas

* **Cliente:**
    * `id_cliente`: Identificador único do cliente.
    * `tipo_cliente`: Indica se o cliente é pessoa física (PF) ou jurídica (PJ).
    * `nome`: Nome do cliente.
    * `cpf`: CPF do cliente (para PF).
    * `cnpj`: CNPJ do cliente (para PJ).
    * `endereco`: Endereço do cliente.
    * `telefone`: Telefone do cliente.
    * `email`: Email do cliente.

* **Pagamento:**
    * `id_pagamento`: Identificador único do pagamento.
    * `id_cliente`: Chave estrangeira referenciando a tabela Cliente.
    * `tipo_pagamento`: Tipo de pagamento (ex: cartão de crédito, boleto).
    * `numero_cartao`: Número do cartão de crédito.
    * `data_validade`: Data de validade do cartão de crédito.

* **Entrega:**
    * `id_entrega`: Identificador único da entrega.
    * `id_cliente`: Chave estrangeira referenciando a tabela Cliente.
    * `status`: Status da entrega (ex: em trânsito, entregue).
    * `codigo_rastreio`: Código de rastreio da entrega.

## Relacionamentos

* Um cliente pode ter múltiplos pagamentos.
* Um cliente pode ter múltiplas entregas.
