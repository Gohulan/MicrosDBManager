# Micros DB Manager

In Oracle Micros Simphony 19.5 and earlier versions client databases were in Microsoft SQL Express, but from version 19.6 onwards, they have changed to MySQL 8.0. If you proceed with the default installation, it will install the clients in MySQL. When it comes to troubleshooting clients our previous MSSQL scripts don't work. Therefore, I have deployed an application to drop client datastore or check and posting databases if necessary. Below is the application you can use to perform this task. While doing so, it will take a backup of the databases to the 'C:/Backup' folder with the current date and time stamp. The username and password will be the same as whatever you are configuring in the property parameters in Oracle Micros Simphony. Please feel free to use this application and let me know your thoughts and suggestions to make it more effective for Oracle F&B consultants.

# Features
Backup Databases: Create backups of Micros Simphony client databases with a timestamp appended to the filename.
Drop Databases: Drop Micros Simphony client databases if required for troubleshooting or migration purposes.

# Usage
1) Download and Extract the application to client workstation
2) Run this application as an Administrator in Simphony POS Client (19.6 or later).
3) It will check if the Simphony client is running or not.
4) If it's running, it will ask to close or kill the servicehost.
5) Once killed, it will prompt to enter the username and password, which are the default MySQL username and password. If you do not remember, please reset it in Simphony >> Property parameters >> Admin user and password.
6) Once logged in successfully, it will show the available databases. We are only going to deal with Simphony CheckandPosting (in CAPS) or Datastore DB in each client.
7) Before dropping, please make sure all checks have been closed and posted, as you are unable to revert it back once it's dropped.
8) Select the database you need to drop.
9) Please only select either CheckPosting or Datastore; do not drop other databases since those are system databases and it will cause issues in the system.
10) Once you select the drop option, it will automatically backup the databases to the 'C:/Backup' folder with the current date and time stamp, and then drop them.
11) Once dropped successfully, exit the application and run the servicehost again. It will automatically start and recreate the database.

# Download MicrosDBManager 

Download Link - https://github.com/Gohulan/MicrosDBManager/raw/main/MicrosDBManager.zip

# Deploying Microsoft SQL Server Express on Microsoft Windows Devices

Go to My Oracle Support, logon and click the Patches & Updates tab, and then search for the CAL package for your version of Microsoft SQL Server Express: Download the CAL package (the patch ID is shown in parenthesis) for your version of Microsoft SQL Server Express:

For SQL Server Express 2016, search for and download patch number 35069532.

For SQL Server Express 2014, search for and download patch number 34362472.

Once the SQL Server Express CAL package file is downloaded, perform the following steps:

Using CAL, install the SQL Server Express Database package on the workstations.

Install the Service Host Download CAL Package.

Install the Service Host.

Deploy the CAL packages as described in CAL Package Deployment and CAL on Workstations.

See Configuring CAL Packages for more information about uploading Custom CAL packages to your system.


