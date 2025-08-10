# Process Flows

## Purchase Flow
```mermaid
flowchart LR
A[Start] --> B[Add Items]
B --> C[Apply Discount]
C --> D{Payment Method?}
D -->|Card/TokenFlex/Cash/POS| E[Process Payment]
E --> F{Success?}
F -->|Yes| G[Create Order]
F -->|No| D
G --> H[Generate Receipt]
H --> I[End]
```

## Refund Flow
```mermaid
flowchart LR
A[Refund Request] --> B[Find Order]
B --> C{Eligible?}
C -->|Yes| D[Create Refund Record]
D --> E[Update Revenue (-)]
E --> F[End]
C -->|No| X[Reject]
```
