## Description
Extend BestDealDBMongo in order to allow the customer to support the following features/functionalities:
1. Search Auto-Completion

## Installation, Compliation and Execution
- Unzip the compressed file.
- Put unzipped folder "BestDealDBMongoAC" under Tomcat's webapp path (%TOMCAT_HOME\webapps).
- All source codes are under the folder \BestDealDBMongoAC\WEB-INF\classes. In case you need to recompile, open command prompt window, navigate to %TOMCAT_HOME\webapps\BestDealDBMongoAC\WEB-INF\classes and issue the javac command.
- Make sure MySQL database is setup and running correctly;
- Make sure an database called "LocalDB" has been created previously. If not, issue "CREATE DATABASE LocalDB;" command in MySQL Workbench or change the database name to any existing databases in file context.xml under %TOMCAT_HOME\webapps\BestDealDBMongoAC\META-INF\
- Make sure MongoDB is setup and running correctly;
- Include the MySQL Java connector (mysql-connector-java-%VERSION-bin.jar) and the MongoDB Java driver (mongo-java-driver-%VERSION.jar) in %TOMCAT_HOME\lib;
- Launch Tomcat server, the servlet application now can be accessed via http://localhost/BestDealDBMongoAC/

## Notes
- For testing purpose, 3 users will be created upon lanuching. These users are:
    1. username = "aa", password = "aa", type = "Customer";
    2. username = "as", password = "as", type = "Salesman";
    3. username = "ad", password = "ad", type = "Store Manager".
You can also create your own user accounts as usual.
- In case needs to move the "BestDeal" folder into different location or change its name, you can simply modified the path information by editing Properties.java. There are 6 global attributes defined in that file:
    1. TOMCAT_HOME: defines the Tomcat installation location;
    2. WEBAPP_PATH: defines location of webapps folder;
    3. PROJECT_PATH: defines location of BestDeal folder;
    4. PRODUCT_CATALOG_PATH: defines the name of product catalog XML file;
    5. USER_DETAILS_PATH: defines the name of user details file;
    6. PAYMENT_DETAILS_PATH: defines the name of payment details file.
