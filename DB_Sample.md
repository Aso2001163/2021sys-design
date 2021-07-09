# データベース詳細
## d_purchase
|属性名|型|PK|NN|FK|
|:-----|:-----|:-----|:-----:|:-----:|
|order_id|bigint(20)|○|○||
|customer_code|varchar(50)||○||
|purchase|date||○||
|total_price|int(11)||○||

## d_purchase_detail
|order_id|bigint(20)|○|○||
|customer_code|varchar(50)||○||
|purchase|date||○||
|total_price|int(11)||○||






