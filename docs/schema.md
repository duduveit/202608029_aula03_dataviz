# 📊 Esquema de Dados - Banco OLIST

## Informações Gerais

| Informação | Valor |
|------------|-------|
| **Banco de Dados** | PostgreSQL 18.6 |
| **Host** | yamanote.proxy.rlwy.net:56714 |
| **Database** | olist |
| **Total de Tabelas** | 15 |
| **Data da Documentação** | 29/08/2026 |

## 📑 Índice de Tabelas

1. [dim_cliente_scd2](#dim_cliente_scd2)
2. [dim_data](#dim_data)
3. [dim_produto](#dim_produto)
4. [dim_vendedor](#dim_vendedor)
5. [fato_item](#fato_item)
6. [fato_pagamento](#fato_pagamento)
7. [olist_customers](#olist_customers)
8. [olist_geolocation](#olist_geolocation)
9. [olist_order_items](#olist_order_items)
10. [olist_order_payments](#olist_order_payments)
11. [olist_order_reviews](#olist_order_reviews)
12. [olist_orders](#olist_orders)
13. [olist_products](#olist_products)
14. [olist_sellers](#olist_sellers)
15. [product_category_name_translation](#product_category_name_translation)

---

## 📈 Estatísticas Gerais

| Tabela | Tamanho em Disco |
|--------|------------------|
| olist_geolocation | 75 MB |
| olist_order_reviews | 30 MB |
| olist_order_items | 25 MB |
| olist_orders | 23 MB |
| olist_customers | 17 MB |
| olist_order_payments | 15 MB |
| olist_products | 5464 kB |
| olist_sellers | 504 kB |
| product_category_name_translation | 32 kB |

## dim_cliente_scd2

**Descrição**: Tabela de dados do sistema OLIST

### Estatísticas

- **Registros**: 96,355
- **Colunas**: 18
- **Índices**: 0
- **Constraints**: 0
- **Chaves Estrangeiras**: 0

### Colunas

| # | Nome | Tipo | Nullable | Default |
|---|------|------|----------|----------|
| 1 | `sk_cliente` | bigint | ✓ SIM | — |
| 1 | `sk_cliente` | bigint | ✓ SIM | — |
| 2 | `customer_unique_id` | text | ✓ SIM | — |
| 2 | `customer_unique_id` | text | ✓ SIM | — |
| 3 | `versao` | integer | ✓ SIM | — |
| 3 | `versao` | integer | ✓ SIM | — |
| 4 | `customer_zip_code_prefix` | integer | ✓ SIM | — |
| 4 | `customer_zip_code_prefix` | integer | ✓ SIM | — |
| 5 | `customer_city` | text | ✓ SIM | — |
| 5 | `customer_city` | text | ✓ SIM | — |
| 6 | `customer_state` | character | ✓ SIM | — |
| 6 | `customer_state` | character | ✓ SIM | — |
| 7 | `valid_from` | timestamp without time zone | ✓ SIM | — |
| 7 | `valid_from` | timestamp without time zone | ✓ SIM | — |
| 8 | `valid_to` | timestamp without time zone | ✓ SIM | — |
| 8 | `valid_to` | timestamp without time zone | ✓ SIM | — |
| 9 | `is_current` | boolean | ✓ SIM | — |
| 9 | `is_current` | boolean | ✓ SIM | — |

### Amostra de Dados

```json
{"sk_cliente": 1, "customer_unique_id": "0000366f3b9a7992bf8c76cfdf3221e2", "versao": 1, "customer_zip_code_prefix": 7787, "customer_city": "cajamar", "customer_state": "SP", "valid_from": datetime.datetime(2018, 5, 10, 10, 56, 27), "valid_to": None, "is_current": True}
{"sk_cliente": 2, "customer_unique_id": "0000b849f77a49e4a4ce2b2a4ca5be3f", "versao": 1, "customer_zip_code_prefix": 6053, "customer_city": "osasco", "customer_state": "SP", "valid_from": datetime.datetime(2018, 5, 7, 11, 11, 27), "valid_to": None, "is_current": True}
{"sk_cliente": 3, "customer_unique_id": "0000f46a3911fa3c0805444483337064", "versao": 1, "customer_zip_code_prefix": 88115, "customer_city": "sao jose", "customer_state": "SC", "valid_from": datetime.datetime(2017, 3, 10, 21, 5, 3), "valid_to": None, "is_current": True}
```

---

## dim_data

**Descrição**: Tabela de dados do sistema OLIST

### Estatísticas

- **Registros**: 774
- **Colunas**: 30
- **Índices**: 0
- **Constraints**: 0
- **Chaves Estrangeiras**: 0

### Colunas

| # | Nome | Tipo | Nullable | Default |
|---|------|------|----------|----------|
| 1 | `sk_data` | integer | ✓ SIM | — |
| 1 | `sk_data` | integer | ✓ SIM | — |
| 1 | `sk_data` | integer | ✓ SIM | — |
| 2 | `data` | date | ✓ SIM | — |
| 2 | `data` | date | ✓ SIM | — |
| 2 | `data` | date | ✓ SIM | — |
| 3 | `ano` | integer | ✓ SIM | — |
| 3 | `ano` | integer | ✓ SIM | — |
| 3 | `ano` | integer | ✓ SIM | — |
| 4 | `trimestre` | integer | ✓ SIM | — |
| 4 | `trimestre` | integer | ✓ SIM | — |
| 4 | `trimestre` | integer | ✓ SIM | — |
| 5 | `mes_numero` | integer | ✓ SIM | — |
| 5 | `mes_numero` | integer | ✓ SIM | — |
| 5 | `mes_numero` | integer | ✓ SIM | — |
| 6 | `ano_mes` | text | ✓ SIM | — |
| 6 | `ano_mes` | text | ✓ SIM | — |
| 6 | `ano_mes` | text | ✓ SIM | — |
| 7 | `dia_mes` | integer | ✓ SIM | — |
| 7 | `dia_mes` | integer | ✓ SIM | — |
| 7 | `dia_mes` | integer | ✓ SIM | — |
| 8 | `dia_semana_numero` | integer | ✓ SIM | — |
| 8 | `dia_semana_numero` | integer | ✓ SIM | — |
| 8 | `dia_semana_numero` | integer | ✓ SIM | — |
| 9 | `dia_semana_nome` | text | ✓ SIM | — |
| 9 | `dia_semana_nome` | text | ✓ SIM | — |
| 9 | `dia_semana_nome` | text | ✓ SIM | — |
| 10 | `fim_de_semana` | boolean | ✓ SIM | — |
| 10 | `fim_de_semana` | boolean | ✓ SIM | — |
| 10 | `fim_de_semana` | boolean | ✓ SIM | — |

### Amostra de Dados

```json
{"sk_data": 20160904, "data": datetime.date(2016, 9, 4), "ano": 2016, "trimestre": 3, "mes_numero": 9, "ano_mes": "2016-09", "dia_mes": 4, "dia_semana_numero": 7, "dia_semana_nome": "Sunday", "fim_de_semana": True}
{"sk_data": 20160905, "data": datetime.date(2016, 9, 5), "ano": 2016, "trimestre": 3, "mes_numero": 9, "ano_mes": "2016-09", "dia_mes": 5, "dia_semana_numero": 1, "dia_semana_nome": "Monday", "fim_de_semana": False}
{"sk_data": 20160906, "data": datetime.date(2016, 9, 6), "ano": 2016, "trimestre": 3, "mes_numero": 9, "ano_mes": "2016-09", "dia_mes": 6, "dia_semana_numero": 2, "dia_semana_nome": "Tuesday", "fim_de_semana": False}
```

---

## dim_produto

**Descrição**: Tabela de dados do sistema OLIST

### Estatísticas

- **Registros**: 32,951
- **Colunas**: 22
- **Índices**: 0
- **Constraints**: 0
- **Chaves Estrangeiras**: 0

### Colunas

| # | Nome | Tipo | Nullable | Default |
|---|------|------|----------|----------|
| 1 | `sk_produto` | bigint | ✓ SIM | — |
| 1 | `sk_produto` | bigint | ✓ SIM | — |
| 2 | `product_id` | text | ✓ SIM | — |
| 2 | `product_id` | text | ✓ SIM | — |
| 3 | `categoria` | text | ✓ SIM | — |
| 3 | `categoria` | text | ✓ SIM | — |
| 4 | `categoria_origem` | text | ✓ SIM | — |
| 4 | `categoria_origem` | text | ✓ SIM | — |
| 5 | `nome_tamanho` | integer | ✓ SIM | — |
| 5 | `nome_tamanho` | integer | ✓ SIM | — |
| 6 | `descricao_tamanho` | integer | ✓ SIM | — |
| 6 | `descricao_tamanho` | integer | ✓ SIM | — |
| 7 | `fotos_quantidade` | integer | ✓ SIM | — |
| 7 | `fotos_quantidade` | integer | ✓ SIM | — |
| 8 | `peso_g` | integer | ✓ SIM | — |
| 8 | `peso_g` | integer | ✓ SIM | — |
| 9 | `comprimento_cm` | integer | ✓ SIM | — |
| 9 | `comprimento_cm` | integer | ✓ SIM | — |
| 10 | `altura_cm` | integer | ✓ SIM | — |
| 10 | `altura_cm` | integer | ✓ SIM | — |
| 11 | `largura_cm` | integer | ✓ SIM | — |
| 11 | `largura_cm` | integer | ✓ SIM | — |

### Amostra de Dados

```json
{"sk_produto": 1, "product_id": "00066f42aeeb9f3007548bb9d3f33c38", "categoria": "perfumery", "categoria_origem": "perfumaria", "nome_tamanho": 53, "descricao_tamanho": 596, "fotos_quantidade": 6, "peso_g": 300, "comprimento_cm": 20, "altura_cm": 16, "largura_cm": 16}
{"sk_produto": 2, "product_id": "00088930e925c41fd95ebfe695fd2655", "categoria": "auto", "categoria_origem": "automotivo", "nome_tamanho": 56, "descricao_tamanho": 752, "fotos_quantidade": 4, "peso_g": 1225, "comprimento_cm": 55, "altura_cm": 10, "largura_cm": 26}
{"sk_produto": 3, "product_id": "0009406fd7479715e4bef61dd91f2462", "categoria": "bed_bath_table", "categoria_origem": "cama_mesa_banho", "nome_tamanho": 50, "descricao_tamanho": 266, "fotos_quantidade": 2, "peso_g": 300, "comprimento_cm": 45, "altura_cm": 15, "largura_cm": 35}
```

---

## dim_vendedor

**Descrição**: Tabela de dados do sistema OLIST

### Estatísticas

- **Registros**: 3,095
- **Colunas**: 10
- **Índices**: 0
- **Constraints**: 0
- **Chaves Estrangeiras**: 0

### Colunas

| # | Nome | Tipo | Nullable | Default |
|---|------|------|----------|----------|
| 1 | `sk_vendedor` | bigint | ✓ SIM | — |
| 1 | `sk_vendedor` | bigint | ✓ SIM | — |
| 2 | `seller_id` | text | ✓ SIM | — |
| 2 | `seller_id` | text | ✓ SIM | — |
| 3 | `seller_zip_code_prefix` | integer | ✓ SIM | — |
| 3 | `seller_zip_code_prefix` | integer | ✓ SIM | — |
| 4 | `seller_city` | text | ✓ SIM | — |
| 4 | `seller_city` | text | ✓ SIM | — |
| 5 | `seller_state` | character(2) | ✓ SIM | — |
| 5 | `seller_state` | character(2) | ✓ SIM | — |

### Amostra de Dados

```json
{"sk_vendedor": 1, "seller_id": "0015a82c2db000af6aaaf3ae2ecb0532", "seller_zip_code_prefix": 9080, "seller_city": "santo andre", "seller_state": "SP"}
{"sk_vendedor": 2, "seller_id": "001cca7ae9ae17fb1caed9dfb1094831", "seller_zip_code_prefix": 29156, "seller_city": "cariacica", "seller_state": "ES"}
{"sk_vendedor": 3, "seller_id": "001e6ad469a905060d959994f1b41e4f", "seller_zip_code_prefix": 24754, "seller_city": "sao goncalo", "seller_state": "RJ"}
```

---

## fato_item

**Descrição**: Tabela de dados do sistema OLIST

### Estatísticas

- **Registros**: 112,650
- **Colunas**: 26
- **Índices**: 0
- **Constraints**: 0
- **Chaves Estrangeiras**: 0

### Colunas

| # | Nome | Tipo | Nullable | Default |
|---|------|------|----------|----------|
| 1 | `nk_item_pedido` | text | ✓ SIM | — |
| 1 | `nk_item_pedido` | text | ✓ SIM | — |
| 2 | `order_id` | text | ✓ SIM | — |
| 2 | `order_id` | text | ✓ SIM | — |
| 3 | `order_item_id` | integer | ✓ SIM | — |
| 3 | `order_item_id` | integer | ✓ SIM | — |
| 4 | `sk_data_compra` | integer | ✓ SIM | — |
| 4 | `sk_data_compra` | integer | ✓ SIM | — |
| 5 | `sk_cliente` | bigint | ✓ SIM | — |
| 5 | `sk_cliente` | bigint | ✓ SIM | — |
| 6 | `sk_produto` | bigint | ✓ SIM | — |
| 6 | `sk_produto` | bigint | ✓ SIM | — |
| 7 | `sk_vendedor` | bigint | ✓ SIM | — |
| 7 | `sk_vendedor` | bigint | ✓ SIM | — |
| 8 | `order_status` | text | ✓ SIM | — |
| 8 | `order_status` | text | ✓ SIM | — |
| 9 | `order_purchase_timestamp` | timestamp without time zone | ✓ SIM | — |
| 9 | `order_purchase_timestamp` | timestamp without time zone | ✓ SIM | — |
| 10 | `shipping_limit_date` | timestamp without time zone | ✓ SIM | — |
| 10 | `shipping_limit_date` | timestamp without time zone | ✓ SIM | — |
| 11 | `preco` | numeric | ✓ SIM | — |
| 11 | `preco` | numeric | ✓ SIM | — |
| 12 | `frete` | numeric | ✓ SIM | — |
| 12 | `frete` | numeric | ✓ SIM | — |
| 13 | `valor_item` | numeric | ✓ SIM | — |
| 13 | `valor_item` | numeric | ✓ SIM | — |

### Amostra de Dados

```json
{"nk_item_pedido": "00010242fe8c5a6d1ba2dd792cb16214-01", "order_id": "00010242fe8c5a6d1ba2dd792cb16214", "order_item_id": 1, "sk_data_compra": 20170913, "sk_cliente": 50882, "sk_produto": 8629, "sk_vendedor": 855, "order_status": "delivered", "order_purchase_timestamp": datetime.datetime(2017, 9, 13, 8, 59, 2), "shipping_limit_date": datetime.datetime(2017, 9, 19, 9, 45, 35), "preco": Decimal("58.90"), "frete": Decimal("13.29"), "valor_item": Decimal("72.19")}
{"nk_item_pedido": "00018f77f2f0320c557190d7a144bdd3-01", "order_id": "00018f77f2f0320c557190d7a144bdd3", "order_item_id": 1, "sk_data_compra": 20170426, "sk_cliente": 88604, "sk_produto": 29598, "sk_vendedor": 2679, "order_status": "delivered", "order_purchase_timestamp": datetime.datetime(2017, 4, 26, 10, 53, 6), "shipping_limit_date": datetime.datetime(2017, 5, 3, 11, 5, 13), "preco": Decimal("239.90"), "frete": Decimal("19.93"), "valor_item": Decimal("259.83")}
{"nk_item_pedido": "000229ec398224ef6ca0657da4fc703e-01", "order_id": "000229ec398224ef6ca0657da4fc703e", "order_item_id": 1, "sk_data_compra": 20180114, "sk_cliente": 21199, "sk_produto": 25668, "sk_vendedor": 1118, "order_status": "delivered", "order_purchase_timestamp": datetime.datetime(2018, 1, 14, 14, 33, 31), "shipping_limit_date": datetime.datetime(2018, 1, 18, 14, 48, 30), "preco": Decimal("199.00"), "frete": Decimal("17.87"), "valor_item": Decimal("216.87")}
```

---

## fato_pagamento

**Descrição**: Tabela de dados do sistema OLIST

### Estatísticas

- **Registros**: 103,886
- **Colunas**: 16
- **Índices**: 0
- **Constraints**: 0
- **Chaves Estrangeiras**: 0

### Colunas

| # | Nome | Tipo | Nullable | Default |
|---|------|------|----------|----------|
| 1 | `nk_pagamento` | text | ✓ SIM | — |
| 1 | `nk_pagamento` | text | ✓ SIM | — |
| 2 | `order_id` | text | ✓ SIM | — |
| 2 | `order_id` | text | ✓ SIM | — |
| 3 | `payment_sequential` | integer | ✓ SIM | — |
| 3 | `payment_sequential` | integer | ✓ SIM | — |
| 4 | `sk_data_compra` | integer | ✓ SIM | — |
| 4 | `sk_data_compra` | integer | ✓ SIM | — |
| 5 | `sk_cliente` | bigint | ✓ SIM | — |
| 5 | `sk_cliente` | bigint | ✓ SIM | — |
| 6 | `payment_type` | text | ✓ SIM | — |
| 6 | `payment_type` | text | ✓ SIM | — |
| 7 | `payment_installments` | integer | ✓ SIM | — |
| 7 | `payment_installments` | integer | ✓ SIM | — |
| 8 | `valor_pagamento` | numeric | ✓ SIM | — |
| 8 | `valor_pagamento` | numeric | ✓ SIM | — |

### Amostra de Dados

```json
{"nk_pagamento": "00010242fe8c5a6d1ba2dd792cb16214-01", "order_id": "00010242fe8c5a6d1ba2dd792cb16214", "payment_sequential": 1, "sk_data_compra": 20170913, "sk_cliente": 50882, "payment_type": "credit_card", "payment_installments": 2, "valor_pagamento": Decimal("72.19")}
{"nk_pagamento": "00018f77f2f0320c557190d7a144bdd3-01", "order_id": "00018f77f2f0320c557190d7a144bdd3", "payment_sequential": 1, "sk_data_compra": 20170426, "sk_cliente": 88604, "payment_type": "credit_card", "payment_installments": 3, "valor_pagamento": Decimal("259.83")}
{"nk_pagamento": "000229ec398224ef6ca0657da4fc703e-01", "order_id": "000229ec398224ef6ca0657da4fc703e", "payment_sequential": 1, "sk_data_compra": 20180114, "sk_cliente": 21199, "payment_type": "credit_card", "payment_installments": 5, "valor_pagamento": Decimal("216.87")}
```

---

## olist_customers

**Descrição**: Tabela de dados do sistema OLIST

### Estatísticas

- **Registros**: 99,441
- **Colunas**: 5
- **Índices**: 1
- **Constraints**: 6
- **Chaves Estrangeiras**: 0

### Colunas

| # | Nome | Tipo | Nullable | Default |
|---|------|------|----------|----------|
| 1 | `customer_id` | text | ✗ NÃO | — |
| 2 | `customer_unique_id` | text | ✗ NÃO | — |
| 3 | `customer_zip_code_prefix` | integer | ✗ NÃO | — |
| 4 | `customer_city` | text | ✗ NÃO | — |
| 5 | `customer_state` | character(2) | ✗ NÃO | — |

### Constraints

- **customers_customer_id_not_null** (CHECK)
- **customers_customer_unique_id_not_null** (CHECK)
- **customers_customer_zip_code_prefix_not_null** (CHECK)
- **customers_customer_city_not_null** (CHECK)
- **customers_customer_state_not_null** (CHECK)
- **customers_pkey** (PRIMARY KEY)

### Índices

```sql
CREATE UNIQUE INDEX customers_pkey ON public.olist_customers USING btree (customer_id)
```

### Amostra de Dados

```json
{"customer_id": "06b8999e2fba1a1fbc88172c00ba8bc7", "customer_unique_id": "861eff4711a542e4b93843c6dd7febb0", "customer_zip_code_prefix": 14409, "customer_city": "franca", "customer_state": "SP"}
{"customer_id": "18955e83d337fd6b2def6b18a428ac77", "customer_unique_id": "290c77bc529b7ac935b93aa66c333dc3", "customer_zip_code_prefix": 9790, "customer_city": "sao bernardo do campo", "customer_state": "SP"}
{"customer_id": "4e7b3e00288586ebd08712fdd0374a03", "customer_unique_id": "060e732b5b29e8181a18229c7b0b2b5e", "customer_zip_code_prefix": 1151, "customer_city": "sao paulo", "customer_state": "SP"}
```

---

## olist_geolocation

**Descrição**: Tabela de dados do sistema OLIST

### Estatísticas

- **Registros**: 1,000,163
- **Colunas**: 5
- **Índices**: 1
- **Constraints**: 5
- **Chaves Estrangeiras**: 0

### Colunas

| # | Nome | Tipo | Nullable | Default |
|---|------|------|----------|----------|
| 1 | `geolocation_zip_code_prefix` | integer | ✗ NÃO | — |
| 2 | `geolocation_lat` | double precision | ✗ NÃO | — |
| 3 | `geolocation_lng` | double precision | ✗ NÃO | — |
| 4 | `geolocation_city` | text | ✗ NÃO | — |
| 5 | `geolocation_state` | character(2) | ✗ NÃO | — |

### Constraints

- **olist_geolocation_geolocation_zip_code_prefix_not_null** (CHECK)
- **olist_geolocation_geolocation_lat_not_null** (CHECK)
- **olist_geolocation_geolocation_lng_not_null** (CHECK)
- **olist_geolocation_geolocation_city_not_null** (CHECK)
- **olist_geolocation_geolocation_state_not_null** (CHECK)

### Índices

```sql
CREATE INDEX olist_geolocation_geolocation_zip_code_prefix_idx ON public.olist_geolocation USING btree (geolocation_zip_code_prefix)
```

### Amostra de Dados

```json
{"geolocation_zip_code_prefix": 1532, "geolocation_lat": -23.568370637803664, "geolocation_lng": -46.637353325148574, "geolocation_city": "sao paulo", "geolocation_state": "SP"}
{"geolocation_zip_code_prefix": 1552, "geolocation_lat": -23.571955068555592, "geolocation_lng": -46.61119233625707, "geolocation_city": "sao paulo", "geolocation_state": "SP"}
{"geolocation_zip_code_prefix": 1508, "geolocation_lat": -23.56282875491954, "geolocation_lng": -46.63808720260835, "geolocation_city": "sao paulo", "geolocation_state": "SP"}
```

---

## olist_order_items

**Descrição**: Tabela de dados do sistema OLIST

### Estatísticas

- **Registros**: 112,650
- **Colunas**: 7
- **Índices**: 1
- **Constraints**: 11
- **Chaves Estrangeiras**: 3

### Colunas

| # | Nome | Tipo | Nullable | Default |
|---|------|------|----------|----------|
| 1 | `order_id` | text | ✗ NÃO | — |
| 2 | `order_item_id` | integer | ✗ NÃO | — |
| 3 | `product_id` | text | ✗ NÃO | — |
| 4 | `seller_id` | text | ✗ NÃO | — |
| 5 | `shipping_limit_date` | timestamp without time zone | ✗ NÃO | — |
| 6 | `price` | numeric | ✗ NÃO | — |
| 7 | `freight_value` | numeric | ✗ NÃO | — |

### Constraints

- **order_items_order_id_not_null** (CHECK)
- **order_items_order_item_id_not_null** (CHECK)
- **order_items_product_id_not_null** (CHECK)
- **order_items_seller_id_not_null** (CHECK)
- **order_items_shipping_limit_date_not_null** (CHECK)
- **order_items_price_not_null** (CHECK)
- **order_items_freight_value_not_null** (CHECK)
- **order_items_pkey** (PRIMARY KEY)
- **order_items_order_id_fkey** (FOREIGN KEY)
- **order_items_product_id_fkey** (FOREIGN KEY)
- **order_items_seller_id_fkey** (FOREIGN KEY)

### Relacionamentos (Chaves Estrangeiras)

- `order_id` → `olist_orders.order_id`
- `product_id` → `olist_products.product_id`
- `seller_id` → `olist_sellers.seller_id`

### Índices

```sql
CREATE UNIQUE INDEX order_items_pkey ON public.olist_order_items USING btree (order_id, order_item_id)
```

### Amostra de Dados

```json
{"order_id": "00010242fe8c5a6d1ba2dd792cb16214", "order_item_id": 1, "product_id": "4244733e06e7ecb4970a6e2683c13e61", "seller_id": "48436dade18ac8b2bce089ec2a041202", "shipping_limit_date": datetime.datetime(2017, 9, 19, 9, 45, 35), "price": Decimal("58.90"), "freight_value": Decimal("13.29")}
{"order_id": "00018f77f2f0320c557190d7a144bdd3", "order_item_id": 1, "product_id": "e5f2d52b802189ee658865ca93d83a8f", "seller_id": "dd7ddc04e1b6c2c614352b383efe2d36", "shipping_limit_date": datetime.datetime(2017, 5, 3, 11, 5, 13), "price": Decimal("239.90"), "freight_value": Decimal("19.93")}
{"order_id": "000229ec398224ef6ca0657da4fc703e", "order_item_id": 1, "product_id": "c777355d18b72b67abbeef9df44fd0fd", "seller_id": "5b51032eddd242adc84c38acab88f23d", "shipping_limit_date": datetime.datetime(2018, 1, 18, 14, 48, 30), "price": Decimal("199.00"), "freight_value": Decimal("17.87")}
```

---

## olist_order_payments

**Descrição**: Tabela de dados do sistema OLIST

### Estatísticas

- **Registros**: 103,886
- **Colunas**: 5
- **Índices**: 1
- **Constraints**: 7
- **Chaves Estrangeiras**: 1

### Colunas

| # | Nome | Tipo | Nullable | Default |
|---|------|------|----------|----------|
| 1 | `order_id` | text | ✗ NÃO | — |
| 2 | `payment_sequential` | integer | ✗ NÃO | — |
| 3 | `payment_type` | text | ✗ NÃO | — |
| 4 | `payment_installments` | integer | ✗ NÃO | — |
| 5 | `payment_value` | numeric | ✗ NÃO | — |

### Constraints

- **order_payments_order_id_not_null** (CHECK)
- **order_payments_payment_sequential_not_null** (CHECK)
- **order_payments_payment_type_not_null** (CHECK)
- **order_payments_payment_installments_not_null** (CHECK)
- **order_payments_payment_value_not_null** (CHECK)
- **order_payments_pkey** (PRIMARY KEY)
- **order_payments_order_id_fkey** (FOREIGN KEY)

### Relacionamentos (Chaves Estrangeiras)

- `order_id` → `olist_orders.order_id`

### Índices

```sql
CREATE UNIQUE INDEX order_payments_pkey ON public.olist_order_payments USING btree (order_id, payment_sequential)
```

### Amostra de Dados

```json
{"order_id": "b81ef226f3fe1789b1e8b2acac839d17", "payment_sequential": 1, "payment_type": "credit_card", "payment_installments": 8, "payment_value": Decimal("99.33")}
{"order_id": "a9810da82917af2d9aefd1278f1dcfa0", "payment_sequential": 1, "payment_type": "credit_card", "payment_installments": 1, "payment_value": Decimal("24.39")}
{"order_id": "25e8ea4e93396b6fa0d3dd708e76c1bd", "payment_sequential": 1, "payment_type": "credit_card", "payment_installments": 1, "payment_value": Decimal("65.71")}
```

---

## olist_order_reviews

**Descrição**: Tabela de dados do sistema OLIST

### Estatísticas

- **Registros**: 99,224
- **Colunas**: 7
- **Índices**: 2
- **Constraints**: 6
- **Chaves Estrangeiras**: 1

### Colunas

| # | Nome | Tipo | Nullable | Default |
|---|------|------|----------|----------|
| 1 | `review_id` | text | ✗ NÃO | — |
| 2 | `order_id` | text | ✗ NÃO | — |
| 3 | `review_score` | integer | ✗ NÃO | — |
| 4 | `review_comment_title` | text | ✓ SIM | — |
| 5 | `review_comment_message` | text | ✓ SIM | — |
| 6 | `review_creation_date` | timestamp without time zone | ✗ NÃO | — |
| 7 | `review_answer_timestamp` | timestamp without time zone | ✗ NÃO | — |

### Constraints

- **order_reviews_review_id_not_null** (CHECK)
- **order_reviews_order_id_not_null** (CHECK)
- **order_reviews_review_score_not_null** (CHECK)
- **order_reviews_review_creation_date_not_null** (CHECK)
- **order_reviews_review_answer_timestamp_not_null** (CHECK)
- **order_reviews_order_id_fkey** (FOREIGN KEY)

### Relacionamentos (Chaves Estrangeiras)

- `order_id` → `olist_orders.order_id`

### Índices

```sql
CREATE INDEX order_reviews_review_id_idx ON public.olist_order_reviews USING btree (review_id)
```
```sql
CREATE INDEX order_reviews_order_id_idx ON public.olist_order_reviews USING btree (order_id)
```

### Amostra de Dados

```json
{"review_id": "7bc2406110b926393aa56f80a40eba40", "order_id": "73fc7af87114b39712e6da79b0a377eb", "review_score": 4, "review_comment_title": None, "review_comment_message": None, "review_creation_date": datetime.datetime(2018, 1, 18, 0, 0), "review_answer_timestamp": datetime.datetime(2018, 1, 18, 21, 46, 59)}
{"review_id": "80e641a11e56f04c1ad469d5645fdfde", "order_id": "a548910a1c6147796b98fdf73dbeba33", "review_score": 5, "review_comment_title": None, "review_comment_message": None, "review_creation_date": datetime.datetime(2018, 3, 10, 0, 0), "review_answer_timestamp": datetime.datetime(2018, 3, 11, 3, 5, 13)}
{"review_id": "228ce5500dc1d8e020d8d1322874b6f0", "order_id": "f9e4b658b201a9f2ecdecbb34bed034b", "review_score": 5, "review_comment_title": None, "review_comment_message": None, "review_creation_date": datetime.datetime(2018, 2, 17, 0, 0), "review_answer_timestamp": datetime.datetime(2018, 2, 18, 14, 36, 24)}
```

---

## olist_orders

**Descrição**: Tabela de dados do sistema OLIST

### Estatísticas

- **Registros**: 99,441
- **Colunas**: 8
- **Índices**: 3
- **Constraints**: 7
- **Chaves Estrangeiras**: 1

### Colunas

| # | Nome | Tipo | Nullable | Default |
|---|------|------|----------|----------|
| 1 | `order_id` | text | ✗ NÃO | — |
| 2 | `customer_id` | text | ✗ NÃO | — |
| 3 | `order_status` | text | ✗ NÃO | — |
| 4 | `order_purchase_timestamp` | timestamp without time zone | ✗ NÃO | — |
| 5 | `order_approved_at` | timestamp without time zone | ✓ SIM | — |
| 6 | `order_delivered_carrier_date` | timestamp without time zone | ✓ SIM | — |
| 7 | `order_delivered_customer_date` | timestamp without time zone | ✓ SIM | — |
| 8 | `order_estimated_delivery_date` | timestamp without time zone | ✗ NÃO | — |

### Constraints

- **orders_order_id_not_null** (CHECK)
- **orders_customer_id_not_null** (CHECK)
- **orders_order_status_not_null** (CHECK)
- **orders_order_purchase_timestamp_not_null** (CHECK)
- **orders_order_estimated_delivery_date_not_null** (CHECK)
- **orders_pkey** (PRIMARY KEY)
- **orders_customer_id_fkey** (FOREIGN KEY)

### Relacionamentos (Chaves Estrangeiras)

- `customer_id` → `olist_customers.customer_id`

### Índices

```sql
CREATE UNIQUE INDEX orders_pkey ON public.olist_orders USING btree (order_id)
```
```sql
CREATE INDEX orders_order_purchase_timestamp_idx ON public.olist_orders USING btree (order_purchase_timestamp)
```
```sql
CREATE INDEX orders_order_status_idx ON public.olist_orders USING btree (order_status)
```

### Amostra de Dados

```json
{"order_id": "e481f51cbdc54678b7cc49136f2d6af7", "customer_id": "9ef432eb6251297304e76186b10a928d", "order_status": "delivered", "order_purchase_timestamp": datetime.datetime(2017, 10, 2, 10, 56, 33), "order_approved_at": datetime.datetime(2017, 10, 2, 11, 7, 15), "order_delivered_carrier_date": datetime.datetime(2017, 10, 4, 19, 55), "order_delivered_customer_date": datetime.datetime(2017, 10, 10, 21, 25, 13), "order_estimated_delivery_date": datetime.datetime(2017, 10, 18, 0, 0)}
{"order_id": "53cdb2fc8bc7dce0b6741e2150273451", "customer_id": "b0830fb4747a6c6d20dea0b8c802d7ef", "order_status": "delivered", "order_purchase_timestamp": datetime.datetime(2018, 7, 24, 20, 41, 37), "order_approved_at": datetime.datetime(2018, 7, 26, 3, 24, 27), "order_delivered_carrier_date": datetime.datetime(2018, 7, 26, 14, 31), "order_delivered_customer_date": datetime.datetime(2018, 8, 7, 15, 27, 45), "order_estimated_delivery_date": datetime.datetime(2018, 8, 13, 0, 0)}
{"order_id": "47770eb9100c2d0c44946d9cf07ec65d", "customer_id": "41ce2a54c0b03bf3443c3d931a367089", "order_status": "delivered", "order_purchase_timestamp": datetime.datetime(2018, 8, 8, 8, 38, 49), "order_approved_at": datetime.datetime(2018, 8, 8, 8, 55, 23), "order_delivered_carrier_date": datetime.datetime(2018, 8, 8, 13, 50), "order_delivered_customer_date": datetime.datetime(2018, 8, 17, 18, 6, 29), "order_estimated_delivery_date": datetime.datetime(2018, 9, 4, 0, 0)}
```

---

## olist_products

**Descrição**: Tabela de dados do sistema OLIST

### Estatísticas

- **Registros**: 32,951
- **Colunas**: 9
- **Índices**: 1
- **Constraints**: 2
- **Chaves Estrangeiras**: 0

### Colunas

| # | Nome | Tipo | Nullable | Default |
|---|------|------|----------|----------|
| 1 | `product_id` | text | ✗ NÃO | — |
| 2 | `product_category_name` | text | ✓ SIM | — |
| 3 | `product_name_lenght` | integer | ✓ SIM | — |
| 4 | `product_description_lenght` | integer | ✓ SIM | — |
| 5 | `product_photos_qty` | integer | ✓ SIM | — |
| 6 | `product_weight_g` | integer | ✓ SIM | — |
| 7 | `product_length_cm` | integer | ✓ SIM | — |
| 8 | `product_height_cm` | integer | ✓ SIM | — |
| 9 | `product_width_cm` | integer | ✓ SIM | — |

### Constraints

- **products_product_id_not_null** (CHECK)
- **products_pkey** (PRIMARY KEY)

### Índices

```sql
CREATE UNIQUE INDEX products_pkey ON public.olist_products USING btree (product_id)
```

### Amostra de Dados

```json
{"product_id": "1e9e8ef04dbcff4541ed26657ea517e5", "product_category_name": "perfumaria", "product_name_lenght": 40, "product_description_lenght": 287, "product_photos_qty": 1, "product_weight_g": 225, "product_length_cm": 16, "product_height_cm": 10, "product_width_cm": 14}
{"product_id": "3aa071139cb16b67ca9e5dea641aaa2f", "product_category_name": "artes", "product_name_lenght": 44, "product_description_lenght": 276, "product_photos_qty": 1, "product_weight_g": 1000, "product_length_cm": 30, "product_height_cm": 18, "product_width_cm": 20}
{"product_id": "96bd76ec8810374ed1b65e291975717f", "product_category_name": "esporte_lazer", "product_name_lenght": 46, "product_description_lenght": 250, "product_photos_qty": 1, "product_weight_g": 154, "product_length_cm": 18, "product_height_cm": 9, "product_width_cm": 15}
```

---

## olist_sellers

**Descrição**: Tabela de dados do sistema OLIST

### Estatísticas

- **Registros**: 3,095
- **Colunas**: 4
- **Índices**: 1
- **Constraints**: 5
- **Chaves Estrangeiras**: 0

### Colunas

| # | Nome | Tipo | Nullable | Default |
|---|------|------|----------|----------|
| 1 | `seller_id` | text | ✗ NÃO | — |
| 2 | `seller_zip_code_prefix` | integer | ✗ NÃO | — |
| 3 | `seller_city` | text | ✗ NÃO | — |
| 4 | `seller_state` | character(2) | ✗ NÃO | — |

### Constraints

- **sellers_seller_id_not_null** (CHECK)
- **sellers_seller_zip_code_prefix_not_null** (CHECK)
- **sellers_seller_city_not_null** (CHECK)
- **sellers_seller_state_not_null** (CHECK)
- **sellers_pkey** (PRIMARY KEY)

### Índices

```sql
CREATE UNIQUE INDEX sellers_pkey ON public.olist_sellers USING btree (seller_id)
```

### Amostra de Dados

```json
{"seller_id": "3442f8959a84dea7ee197c632cb2df15", "seller_zip_code_prefix": 13023, "seller_city": "campinas", "seller_state": "SP"}
{"seller_id": "d1b65fc7debc3361ea86b5f14c68d2e2", "seller_zip_code_prefix": 13844, "seller_city": "mogi guacu", "seller_state": "SP"}
{"seller_id": "ce3ad9de960102d0677a81f5d0bb7b2d", "seller_zip_code_prefix": 20031, "seller_city": "rio de janeiro", "seller_state": "RJ"}
```

---

## product_category_name_translation

**Descrição**: Tabela de dados do sistema OLIST

### Estatísticas

- **Registros**: 71
- **Colunas**: 2
- **Índices**: 1
- **Constraints**: 3
- **Chaves Estrangeiras**: 0

### Colunas

| # | Nome | Tipo | Nullable | Default |
|---|------|------|----------|----------|
| 1 | `product_category_name` | text | ✗ NÃO | — |
| 2 | `product_category_name_english` | text | ✗ NÃO | — |

### Constraints

- **product_category_translation_product_category_name_not_null** (CHECK)
- **product_category_translatio_product_category_name_engl_not_null** (CHECK)
- **product_category_translation_pkey** (PRIMARY KEY)

### Índices

```sql
CREATE UNIQUE INDEX product_category_translation_pkey ON public.product_category_name_translation USING btree (product_category_name)
```

### Amostra de Dados

```json
{"product_category_name": "beleza_saude", "product_category_name_english": "health_beauty"}
{"product_category_name": "informatica_acessorios", "product_category_name_english": "computers_accessories"}
{"product_category_name": "automotivo", "product_category_name_english": "auto"}
```

---

