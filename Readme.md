###Fermers food

To start project need to be installed:
1. JDK v8 or later
2. Maven
3. Npm
4. MySql
 - configuration of DB connection stored in the application.properties file
 - you need to configure your database as provided in config
 - create database via command: `CREATE DATABASE db_fermersFood CHARACTER SET utf8 COLLATE utf8_general_ci`
	   
5. tomcat app server

###To run app use mvn spring-boot:run command or run-> java Application from menu of IDE


###REST DESCRIPTION 
	***ACOUNT***

1. GET   ***/accounts - get All accounts - token Only ADMIN
2. POST  ***/accounts/login - login - `{"email":"email", "password":"password"}` - free access
3. POST  ***/accounts/account -  sing up -` {"email":"email", "password":"password"}` role will be set by default value "USER". Admin have possibilitie to change this role in future 
4. PUT   ***/accounts/account - change pass - `{"email":"email", "password":"password"}` - all authorized users 
5. GET   ***/accounts/account - getAccountInfo -` "token in authorization header"` - all authorized users
6. GET   ***/accounts/account/{id} - delete Account -` "for administrators" token and accountID `for account which should be deleted - only ADMIN  
7. POST  ***/accounts/account/user - update user info for account - ` {fields from user table}+token `- all authorized users
8. GET   ***/accounts/account/user - get user info for account -` token` - all authorized users





