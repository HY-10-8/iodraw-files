```mermaid
sequenceDiagram
    autonumber
    服务器->>+数据库: 执行sql
    activate 数据库
    数据库->>数据库: 执行sql
    数据库->>+服务器: 返回数据/游标

    loop 
        服务器-->服务器: 读取数据到内存并转化成实体类
    end
```