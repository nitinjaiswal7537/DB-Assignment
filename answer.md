Ans 1) The relatiionship between Product and Product_category seemed to have one-to-many relationship as one record from the product_category is related to many record of the product category so thry have one-to-amny relationship.Further he relationship between the "Product" and "Product_Category" entities seems to be established through a foreign key relationship.
In the "Product" table, there is a column named "category_id" which likely serves as a foreign key referencing the "id" column of the "Product_Category" table. This indicates that each product in the "Product" table is associated with a specific category defined in the "Product_Category" table.



Ans 2) We can use foreign key constrain inorder to established referntial intergrity between the two tables using the following sql command:

ALTER TABLE Product
ADD CONSTRAINT fk_product_category
FOREIGN KEY (category_id)
REFERENCES Product_Category(id);

The database management system will make sure that any value added into the "category_id" column of the "Product" table corresponds to a value already present in the "id" column of the "Product_Category" table as a result of this constraint. By preventing orphaned records and preserving data integrity, this makes sure that every product is linked to an appropriate category.
