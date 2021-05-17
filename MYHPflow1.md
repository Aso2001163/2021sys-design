会員登録とログイン

```uml
@startuml
ユーザー -> webサーバー : ログイン
webサーバー -> DBサーバー : 登録データと照合
DBサーバー -> DBサーバー : ログイン処理
DBサーバー -> webサーバー : 認証結果
webサーバー -> ユーザー : 認証結果

activate ユーザー

opt 認証成功
webサーバー -> ユーザー : マイページを表示

else 認証失敗
webサーバー -> ユーザー : 再入力を要求
end

deactivate ユーザー

@enduml
```
