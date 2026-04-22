```mermaid
sequenceDiagram
    autonumber

    participant FE
    participant BE

    FE->>FE: fe
    DSv2-->>Spark: 返回 CustomHudiTable
```