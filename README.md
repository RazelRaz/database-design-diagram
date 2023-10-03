## Prisma Database Migration

This Prisma database migration creates the following tables:

* **categories:** This table stores information about product categories.
* **products:** This table stores information about products.
* **users:** This table stores information about users.
* **customers:** This table stores information about customers.
* **invoices:** This table stores information about invoices.
* **invoice_products:** This table stores information about the products associated with an invoice.

**Relationships**

The following relationships exist between the different tables:

* One category can have many products.
* One product can belong to one category.
* One user can have many customers.
* One customer can belong to one user.
* One user can have many invoices.
* One invoice can belong to one user.
* One invoice can have many products.
* One product can be associated with many invoices.

**onDelete:Restrict**

The `onDelete:Restrict` option is used for all of the foreign key relationships. This prevents orphaned records from being created in the database. For example, if you delete a category, all of the products associated with that category will also be deleted.

**onUpdate:Cascade**

The `onUpdate:Cascade` option is used for all of the foreign key relationships that point to the `users` model. This ensures that all of the records associated with a user are updated if the user's information is changed. For example, if you change the user's name, all of the invoices associated with that user will also have their user name updated.

**Usage**

To use this Prisma database migration, you can run the following command:
