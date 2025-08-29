# Security

Access control and security definitions in sale_order_tag.

## Access Control Lists (ACLs)

Model access permissions defined in:
- **[ir.model.access.csv](../sale_order_tag/security/ir.model.access.csv)**
  - 2 model access rules

## Record Rules

Row-level security rules defined in:

## Security Groups & Configuration

Security groups and permissions defined in:
- **[sale_order_tag_security.xml](../sale_order_tag/security/sale_order_tag_security.xml)**

```mermaid
graph TB
    subgraph "Security Layers"
        A[Users] --> B[Groups]
        B --> C[Access Control Lists]
        C --> D[Models]
        B --> E[Record Rules]
        E --> F[Individual Records]
    end
```

Security files overview:
- **[ir.model.access.csv](../sale_order_tag/security/ir.model.access.csv)**
  - Model access permissions (CRUD rights)
- **[sale_order_tag_security.xml](../sale_order_tag/security/sale_order_tag_security.xml)**
  - Security groups, categories, and XML-based rules

Notes
- Access Control Lists define which groups can access which models
- Record Rules provide row-level security (filter records by user/group)
- Security groups organize users and define permission sets
- All security is enforced at the ORM level by Odoo
