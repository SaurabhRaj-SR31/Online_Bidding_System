# Setup Instructions:

Prerequisites
->Visual Studio 2019 or later: Ensure you have Visual Studio installed on your machine. 
->SQL Server: Install SQL Server for database management. You can download it from here.
->.NET Framework 4.7.2 or later: Make sure the required .NET framework is installed.

#Steps:
Clone the Repository:
Open a command prompt or terminal and run the following command to clone the repository:
git clone https://github.com/SaurabhRaj-SR31/Online_Bidding_System.git

Open the Project in Visual Studio:
Launch Visual Studio.
Navigate to File > Open > Project/Solution.
Select the .sln file located in the cloned repository directory.

Restore NuGet Packages:
Visual Studio should automatically restore the required NuGet packages. If it doesn’t, you can manually restore them by:
Right-clicking on the solution in the Solution Explorer.
Selecting Restore NuGet Packages.

Update the Database Connection String:
Open the Web.config file located in the root of the project.
Locate the <connectionStrings> section and update the connection string to point to your SQL Server instance. It should look something like this:
xml
<connectionStrings>
  <add name="DefaultConnection" connectionString="Server=your_server_name;Database=your_database_name;User Id=your_username;Password=your_password;" providerName="System.Data.SqlClient" />
</connectionStrings>

Apply Database Migrations:
Open the Package Manager Console in Visual Studio (Tools > NuGet Package Manager > Package Manager Console).
Run the following command to apply database migrations and create the necessary tables:

Update-Database

Run the Application:
Press F5 or navigate to Debug > Start Debugging to build and run the application.
The application should open in your default web browser, and you can start using the online bidding website.
