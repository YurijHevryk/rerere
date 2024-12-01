```mermaid
classDiagram
    class SalesTracker {
        - sales_history_listbox
        - product_sales_history_listbox
        + __init__(sales_history_listbox, product_sales_history_listbox)
        + record_sale(customer_name: str, product_name: str, quantity: int, total_price: float)
    }
```