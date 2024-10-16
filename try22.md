```mermaid
classDiagram
    class TreeType {
        -name: str
        -color: str
        -texture: str
        +draw(canvas, x: int, y: int)
    }

    class TreeFactory {
        -_tree_types
        +get_tree_type(name: str, color: str, texture: str): TreeType
    }

    class Tree {
        -x: int
        -y: int
        -tree_type: TreeType
        +draw(canvas)
    }

    class Forest {
        -trees: list
        +plant_tree(x: int, y: int, name: str, color: str, texture: str)
        +draw(canvas)
    }

    TreeType <|-- TreeFactory : uses
    TreeType <|-- Tree : composition
    TreeFactory <|-- Forest : uses
    Tree <|-- Forest : composition
```s