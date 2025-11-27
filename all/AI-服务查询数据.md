```mermaid
sequenceDiagram
    
    服务器->>+数据库驱动: 执行sql
    数据库驱动->>数据库:执行sql

    activate 数据库
    数据库->>数据库: 执行sql
    数据库->>+数据库驱动: 返回数据/游标
    deactivate 数据库

    critical 同步
        loop 
            数据库驱动->>数据库: 请求下一行数据
            数据库->>数据库驱动: 返回数据
        end
        数据库驱动->>服务器: 将数据读入内存
    end

    loop 异步
        数据库驱动->>数据库: 请求下一行数据
        数据库->>数据库驱动: 返回数据
        数据库驱动->>服务器: 将数据读入内存
    end


sequenceDiagram
```