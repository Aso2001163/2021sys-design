```startuml
@startuml



customer       |o-ri-o{    order
pass

order          ||-ri-|{     order_detail 

order_detail    }-do-||     items 

items          }o-le-||     category 


  


@enduml
```
