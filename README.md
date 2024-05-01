# Billing-System
A GUI Based Complete Store Billing System in java that generates Invoice of each sale.
================================================================
Set up billing system server:

Downloading and installing dependencies to the project
1. Download the repository by clicking the green “<> Code” dropdown menu and clicking “Download ZIP”
2. Open the project in an IDE (such as Eclipse)
3. You need to have “com.mysql.jdbc.driver” in your PATH on your device, or you’ll have to add it as a dependency in your project.
To do this, download the connector .jar file from here: https://dev.mysql.com/downloads/connector/j/5.0.html
In the IDE (such as Eclipse), right click on the project.
In the drop down menu click Build Path -> Configure Build Path…
Click on “Classpath”
Click on “Add External JARS…” on the rightside panel
Navigate to where you downloaded the .jar file. For Example: “C:\Users\user1\Downloads\mysql-connector-j-8.4.0\mysql-connector-j-8.4.0.jar”
Click the “mysql-connector-j-8.4.0.jar” file and Click Open
Click “Apply and Close”

Creating and connecting to the database in MySQL
REQUIREMENTS:
MySQL
MySQL Workbench

1. Open MySQL Workbench
2. Open connection in MySQL Connections
3. Write and execute the following queries:

CREATE DATABASE caddey;
USE caddey;
CREATE TABLE users(
	email varchar(255),
	password varchar(255)
);

4. If you have a password on your “root” sql account, you’ll need to add the password into the code.
In your editor (Eclipse), open the file src/DB.java.
Edit line 22 to include your password. The line should look like this:

conn = DriverManager.getConnection("jdbc:mysql://localhost/caddey","root", "");

Put your password in the final quotation marks like this

conn = DriverManager.getConnection("jdbc:mysql://localhost/caddey","root", "[PASSWORD]");

5. You’ll need to add users in MySQL Workbench by interesting records into the “users” table using this command:

INSERT INTO users (email, password)
VALUES (“[username]”, “[password]”);

You can enter more users by repeating this command with different usernames and passwords.

NOTE: an account with the username “admin” is special and has additional privileges in this program.

You should now be able to run the Login.java file and enter your username and password to access the program.

Creating the “stock” and “sale” databases
1. We’ll need to create a table named “stock” with the column names “ProductID”, “Detail”, “Company”, and “Quantity”. To create this table, execute the following command in MySQL Workbench:

CREATE TABLE stock(
	ProductID varchar(255),
	Detail varchar(255),
	Company varchar(255),
	Quantity int
);

2. Create the table named “sale” with the column names “ProductID”, “Date”, “Company”,and “Payment.” Enter the following command into MySQL Workbench:

CREATE TABLE stock(
	Date varchar(255),
	ProductID varchar(255),
	Company varchar(255),
	Payment varchar(255)
);

Now with the database set up, you are ready to begin using the program. To run the program, run the Login.java file in you text editor (Eclipse).
