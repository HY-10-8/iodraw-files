```mermaid
sequenceDiagram
    autonumber

    participant FE
    participant BE

    FE->>FE: FE 解析与语义分析
    FE->>FE: FE 生成分布式执行计划
    FE-->>BE: 将z
```