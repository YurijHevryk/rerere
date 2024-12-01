```mermaid
classDiagram
    class CustomerManager {
        - listbox
        - customers : list
        + __init__(listbox)
        + add_customer(name: str, contact: str)
    }
```