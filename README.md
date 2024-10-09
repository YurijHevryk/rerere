```mermaid
classDiagram
  class User {
    + name: String
    + has_access: Boolean
  }
  class ExpensiveResource {
    + __init__()
    + process()
  }
  class ResourceProxy {
    + resource: ExpensiveResource
    + user: User
    + __init__(resource: ExpensiveResource, user: User)
    + process()
  }
  User <-> ResourceProxy
  ResourceProxy --> ExpensiveResource
  note right of User: Represents a user of the system.
  note right of ExpensiveResource: Represents a resource that might be expensive to create or access.
  note right of ResourceProxy: Acts as a gatekeeper for the ExpensiveResource.
```