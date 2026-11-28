# Database Documentation

This document describes the current database setup, role/permission schema, enums, and seeders implemented in the project.

## Database Configuration

- **Connection / Engine:** SQLite (current development setup).
- **Core Application Migrations:** users, cache, and jobs tables.
- **Authorization Tables:** Added via spatie/laravel-permission migration (oles, permissions, model_has_roles, model_has_permissions, and ole_has_permissions).

## Roles and Permissions Design

### Roles (RolesEnum)

- Admin — Full administrative access across platform permissions.
- Vendor — Seller access (SellProducts and BuyProducts).
- User — Standard customer/buyer access (BuyProducts).

### Permissions (PermissionsEnum)

- ApproveVendors — Assigned to Admin. (Note: verify RoleSeeder assignment to confirm all intended roles are synced.)
- SellProducts — Assigned to Vendor and Admin. (Note: verify RoleSeeder assignment to confirm all intended roles are synced.)
- BuyProducts — Assigned to User, Vendor, and Admin. (Note: verify RoleSeeder assignment to confirm all intended roles are synced.)

## Seeders

- RoleSeeder: Creates the Admin, Vendor, and User roles and the ApproveVendors, SellProducts, and BuyProducts permissions, then syncs permissions to roles.
- UserSeeder: Creates sample/default users (User, Vendor, Admin) and assigns their respective roles.
- DatabaseSeeder: Orchestrates RoleSeeder and UserSeeder. (Note: review whether UserSeeder should be guarded or used only for local/development seeding before production.)

## Notes & Future Schema Additions

- This document reflects the current schema and authorization setup only. Product catalog, categories, orders, carts, and checkout tables will be documented as those features are implemented.
