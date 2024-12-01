```mermaid
classDiagram
    class MineralFertilizerTradingApp {
        - root
        - button_style
        - product_name_entry
        - product_price_entry
        - product_quantity_entry
        - customer_name_entry
        - customer_contact_entry
        - product_listbox
        - customer_listbox
        - sale_quantity_entry
        - sales_history_listbox
        - product_sales_history_listbox
        - product_manager
        - customer_manager
        - sales_tracker
        + __init__(root)
        + create_widgets()
        + create_product_frame()
        + create_customer_frame()
        + create_sale_frame()
        + create_history_frames()
        + add_product()
        + add_customer()
        + process_sale()
    }
    MineralFertilizerTradingApp --> ProductManager
    MineralFertilizerTradingApp --> CustomerManager
    MineralFertilizerTradingApp --> SalesTracker
```