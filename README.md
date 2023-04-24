You can run this file with the command 'python app.py' and then access the endpoints at 'http://localhost:5000/', 'http://localhost:5000/ranges', and 'http://localhost:5000/clothing'

This application recommends outdoor clothing based on temperature ranges at a location.

It uses SQLAlchemy to create a db schema with two tables, Clothing and Ranges. They each have a many-to-many relationship via the Recommendations join table.  Each Clothing item can be recommended for multiple Ranges and each Range can 'recommend' multiple Clothing items.

The models.py file shows Ranges and Clothing classes with attributes defined as columns. 

The join table is defined as a table object - hence, the two foreign key columns.

Instances of the Ranges and Clothing classes are created and then added to the database via the 'session' object.... the instances represent the comvination of clothing items and temperature ranges the application recommends to the user.