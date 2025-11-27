```mermaid
sequenceDiagram
    autonumber
    服务器->>+数据库驱动: 执行sql
    数据库驱动->>数据库:执行sql

    activate 数据库
    数据库->>数据库: 执行sql
    数据库->>+数据库驱动: 返回数据/游标
    deactivate 数据库

    loop 
        数据库驱动->>数据库: 请求下一行数据
        数据库->>数据库驱动: 返回数据
        数据库驱动->>服务器: 123
    end
```