```startuml
@startuml

entity "顧客マスタ" as cus {
  *cus_id : number <<generated>>
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






cus      |o-ri-o{    or
or          ||-ri-|{     order_detail 
order_detail    }-do-||     items 
items          }o-le-||     category 


  


@enduml
```
