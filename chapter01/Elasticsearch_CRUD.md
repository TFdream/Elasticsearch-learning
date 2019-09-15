## 文档的基本CRUD与批量操作
| 操作 | 命令 | 备注 |
| ---- | --- | --- |
| Index | PUT myindx/_doc/1 {"user_name":"mike", "comment":"You know, for search"}| Type名约定都用 _doc |
| Create | PUT myindx/_create/1 {"user_name":"mike", "comment":"You know, for search"} <br>POST myindx/_doc (不指定ID，自动生成) {"user_name":"mike", "comment":"You know, for search"}| 如果ID已经存在会失败 |
| GET | GET myindx/_doc/1| |
| Update | POST myindx/_update/1 {"doc":{"user_name":"mike", "comment":"You know, for search"}}| 文档必须已经存在，更新只会对相应对字段做增量更新 |
| Delete | DELETE myindx/_doc/1| |
