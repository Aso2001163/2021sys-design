```startuml
@startuml
!define MASTER_MARK_COLOR Orange 
!define TRANSACTION_MARK_COLOR Blue
 entity "顧客マスタ" as customer <m_customers> <<M,MASTER_MARK_COLOR>> {
        + customer_code [PK]
  --
  pass
  name
  address
  tel
  mail
  del_flag
  reg_date
}

entity "購入テーブル" as order <d_purchase> <<TRANSACTION_MARK_COLOR>>{
  + order_id[PK]
  --
  customer_code[FK]
  purchase_date
  total_price
}






customer      |o-ri-o{    order
order          ||-ri-|{     order_detail 
order_detail    }-do-||     items 
items          }o-le-||     category 


  


@enduml
```
