# Eu Claire Salon 

#### Creating a Web Application, using Database basics with C# for Epicodus 07.28.2022

### By Adrienne Matosich 

## Description

Another C# independent project! We've attached a database using MySql Workbench and implemented Entity Framework to link it to our application. This hair salon application is designed to help salon owners keep track of their clients and stylists. 


## Specifications

**Behavior**: Program will have a homepage where users can choose to view current stylists and clients.
  * Input: User clicks "view stylists"
  * Output: User is taken to a page with a list of stylists

**Behavior**: Program will have a link to add a new stylist on the stylist list page.
  * Input: User clicks "Add a new stylist"
  * Output: User is taken to a form to add a new stylist

**Behavior**: Program will have a link to add a new vendor on the vendor list page.
  * Input: User clicks "Add a new vendor"
  * Output: User is taken to a form to add a new vendor

**Behavior**: Program will return user to the stylist list page after submission of the stylist form.
  * Input: User submits new stylist form
  * Output: User is taken to the stylist list page
 
**Behavior**: Program will have a detail page for each stylist that lists that stylist's clients.
  * Input: User clicks "Adrienne"
  * Output: User is taken to a page with a list of Adrienne's clients

**Behavior**: Program will return user to the stylist detail page after submission of the client form.
  * Input: User submits "add new client"
  * Output: User is taken back to stylist detail page

**Behavior**: Program will allow user to edit or delete a stylist/client.
  * Input: User clicks "Edit/Delete Stylist/Client"
  * Output: User can change/delete name and/or current stylist/client 



## Setup/Installation Requirements

1.  Navigate to the [HairSalon.Solution repository](https://github.com/ampando/HairSalon.Solution) or open your terminal

2. Clone this project using the GitHub button or the command:
`$ git clone https://github.com/ampando/HairSalon.Solution.git`

3. Confirm that MYSQL server is running by opening your terminal and entering the command `mysql -uroot -pepicodus`.

4. Open MySQL Workbench and click on the the `Administration` tab. 

5. Click on `Data Import/Restore` in the left-hand column.

6. Select `Import from Self-Contained File`, and enter the path to adrienne_matosich.sql. An example path could look like this: /Users/yourname/desktop/HairSalon.Solution/adrienne_matosich.sql.

7. Click on the `New` button in the Default Schema to be `Imported To` and for the schema name enter 'adrienne_matosich'.

8. In the drop down menu, select (Dump Structure Only) if you'd like to import only the data structure or (Dump Structure and Data) if you'd like to dump both the structure and data previously entered. 

9. Click the `Start Import` button to finish adding the database.

10. Navigate to the `HairSalon.Solution` directory in your editor of choice, or use [Visual Studio Code](https://code.visualstudio.com/)

11. Within the project, navigate to the HairSalon.Solution directory, and type `dotnet restore`, then `dotnet build`. Once the build is complete, type `dotnet run` into the terminal. Click on the provided local host link in the terminal to view the web application in your browser.

## SQL Schema Query

The SQL commands below can be used with a the SQL manager to create the database for this project:

DROP DATABASE IF EXISTS `adrienne_matosich`;
CREATE DATABASE `adrienne_matosich`;

USE `adrienne_matosich`;

CREATE TABLE `clients` (
  `ClientId` int NOT NULL AUTO_INCREMENT,
  `ClientName` varchar(255) NOT NULL,
  `StylistId` int DEFAULT '0',
  PRIMARY KEY (`ClientId`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

CREATE TABLE `stylists` (
  `StylistId` int NOT NULL AUTO_INCREMENT,
  `StylistName` varchar(255) DEFAULT NULL,
  `Specialty` varchar(255) DEFAULT NULL,
  PRIMARY KEY (`StylistId`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

## appsettings.json

Update your username and password in the appsettings.json file. By default these are set to:
user:root and an [empty password].

## Protecting Your Data

1. In your project's root directory, create an .gitignore file.

2. Add the following to your .gitignore file (this protects your sensitive data).
    DO NOT PROCEED UNTIL YOU COMPLETE THIS STEP!
    * appsettings.json
    * bin/
    * obj/

3. Commit your .gitignore file.

## Known Bugs

The css styling needs more time. 

## Support and Contact Details

If there are any issues or questions, please reach out to me through [my GitHub account](https://github.com/ampando).

## Technologies Used

*  [Visual Studio Code](https://code.visualstudio.com/)
*  [Markdown](https://daringfireball.net/projects/markdown/)
*  [C#](https://docs.microsoft.com/en-us/dotnet/csharp/)
*  [.NET5.0](https://dotnet.microsoft.com/download/dotnet-core/net5.0)
*  [ASP.NET Core MVC](https://docs.microsoft.com/en-us/aspnet/core/mvc/overview?view=aspnetcore-3.1)
*  [Entity FrameWork](https://docs.microsoft.com/en-us/ef/)

### License

*This project uses the following license: [MIT](https://opensource.org/licenses/MIT)*

Copyright(c) 2022  **_Adrienne Matosich_** 