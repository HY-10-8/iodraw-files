```mermaid
sequenceDiagram
    autonumber
    服务器->>+数据库驱动: 执行sql
    数据库驱动->>shu'ju'k

    activate 数据库
    数据库->>数据库: 执行sql
    数据库->>+服务器: 返回数据/游标
    deactivate 数据库

    loop 
        服务器-->服务器: 
    end
```