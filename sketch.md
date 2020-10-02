# [Quick Database Diagrams](https://app.quickdatabasediagrams.com/#/)

## Propritary markdown-style languguage

```mu
Customer
-
customer_id PK int
customer_name string

Credit_Card
-
card_id PK bigint
card_holder FK - Customer.customer_id

Merchant
-
merchant_id PK int
merchant_name string
merchant_category FK >- Merchant_Category.category_id

Merchant_Category
-
category_id PK int
category_name string

Transactions
-
transaction_id PK int
date Date
amount float
card FK >- Credit_Card.card_id
merchant FK >- Merchant.merchant_id
```