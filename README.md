# Sale system
This is a simple multi-user sale system

## Dependencies

## Features
	- User authentication
	- Stock management
	- Clients and providers directory
	- Sales reports
	- Operations reports
	- Shopping cart
	- Credits and pull aparts(Is pull apart correct?)

## Design
### ER Diagram
![ER diagram](/docs/database/db-schema.png)

### Mockup
![ER diagram](/docs/mockup/schema.png)

## Setup
### Database
```sql
-- Create database
CREATE DATABASE sale_system;

-- Create Tables
CREATE TABLE branches(
	id int AUTO_INCREMENT,
	name varchar(20) NOT NULL
	PRIMARY KEY(id)
);


CREATE TABLE users(
	id int AUTO_INCREMENT,
	name varchar(35),
	password varchar(20),
	is_super bit,
	can_discount bit,
	branch_id tinyint,
	PRIMARY KEY(id),
	FOREIGN KEY(branch_id) REFERENCES branches(id) ON DELETE SET NULL
);


```

## License
[MIT License](/LICENSE)
