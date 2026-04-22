```mermaid
sequenceDiagram
    autonumber

    participant FE
    participant BE

    FE->>FE: 分析SQL
    FE-->>Spark: 返回 CustomHudiTable
```