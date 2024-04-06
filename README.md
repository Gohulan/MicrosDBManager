# MicrosDBManager

In Oracle Micros Simphony 19.5 and earlier versions client databases were in Microsoft SQL Express, but from version 19.6 onwards, they have changed to MySQL 8.0. If you proceed with the default installation, it will install the clients in MySQL. When it comes to troubleshooting clients our previous MSSQL scripts don't work. Therefore, I have deployed an application to drop client datastore or check and posting databases if necessary. Below is the application you can use to perform this task. While doing so, it will take a backup of the databases to the 'C:/Backup' folder with the current date and time stamp. The username and password will be the same as whatever you are configuring in the property parameters in Oracle Micros Simphony. Please feel free to use this application and let me know your thoughts and suggestions to make it more effective for Oracle F&B consultants.

# Features
Backup Databases: Create backups of Micros Simphony client databases with a timestamp appended to the filename.
Drop Databases: Drop Micros Simphony client databases if required for troubleshooting or migration purposes.

# Usage
Run the Application: Execute the generated executable file (MicrosDBManager.exe) from the command line or terminal.

Backup Database: To create a backup of a database, run the application and select the option to backup a database. Select the database name when prompted.

Drop Database: To drop a database, run the application and select the option to drop a database. Provide the database name when prompted.



