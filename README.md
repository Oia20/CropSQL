# CropSQL
A game where users learn sql by managing a farm.

The flow of the SQL learning game:

Color Palette:

Glade Green: #5e8d61
Olivine: #a2b780
Cream Can: #f4d35d
Apricot: #e8a073
Matrix: #b0545a



1. Hello welcome to CropSQL, in this game you will learn and use SQL commands and queries to build and manage your farm.

2. Let's start by creating your farm with "CREATE DATABASE" followed by the name of your farm. ex: CREATE DATABASE myFarm; don't forget the semi-colon, this is how sql knows where your command ends.

3. Next lets tell our command line that we are going to be using our farm's database with the "USE" command
CropSQL> USE myFarmName;

4. You need a table to store the crops in your field. Create a table with "CREATE TABLE" followed by the table name, then open a parentheses "("
inside of your table you can specify columns, and what datatype goes into them. This will make more sense later in the game, but for now, lets create a column named Crop with a data type of varchar(20) which is a word with a max of 20 characters. Then an Amount column which takes and int, and a Word column which also takes an int.

CropSQL> CREATE TABLE Crops (
        Crop varchar(20),
        Amount int
        );

5. Oops, it looks like we forgot to add a column for how much our Crops are worth! Not to worry, SQL gives us a command for that. "ALTER TABLE tableName" followed by ADD columnName datatype

CropSQL> ALTER TABLE Crops
CropSQL> ADD Worth int;

6. Lovely now lets view our Crops table! do this with the "SELECT" command followed by "*" which functions as a select all, then "FROM" followed by the tables name.

CropSQL> SELECT * FROM Crops;

7. Next it's time that we plant some crops. Let's start with the worst one of all, Carrots! 
in SQL we do this with the "INSERT INTO" command followed by the table name. Then in parentheses we specify which columns we want to modify, in our case
we want to modify all columns "INSERT INTO Crops (Crop, Amount, Worth)" Then we use the "VALUES ()" command to insert into columns
Let's plant 5 carrots at a Worth of 2.

CropSQL> INSERT INTO Crops (Crop, Amount, Worth)
CropSQL> VALUES (Carrot, 5, 2);