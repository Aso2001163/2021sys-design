```startuml
@startuml

entity "顧客マスタ" as customer <m_customers>
<<M,MASTER_MARK_COLOR>>{
 +customer_code[PK]
  --
  *name : text
  description : text
}

entity "order" as or {
  *or_id : number <<generated>>
  --
  *name : text
  description : text
}






customer      |o-ri-o{    or
or          ||-ri-|{     order_detail 
order_detail    }-do-||     items 
items          }o-le-||     category 


  


@enduml
```
