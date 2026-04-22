```mermaid
sequenceDiagram
    autonumber

    participant FE
    participant BE

    F#->>DSv2: TableProvider.getTable(schema, partitioning, properties)
    DSv2-->>Spark: 返回 CustomHudiTable
```