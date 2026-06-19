
# step-by-step-guide-on-how-to-create-a-database-postgres-in-Linux-server-using-Linux-commands
Data Engineers mostly works with databases so I created one of them using Linux servers following the highlighted steps below:

## 1. Server Access
Log into the server using SSH on port 22.
Host:
159.65.222.96
User:
root

  
## 2. User Creation
Create a Linux user account using the following format:
- Username: your first name + surname initial
- Example: If your name is Jane Doe → JaneD

 
## 3. PostgreSQL Setup
Check if PostgreSQL is installed:
psql --version

If PostgreSQL is not installed, install it.
 
If it is installed, ensure the PostgreSQL service is running and accessible.
 
Also ensure that:
 
- The server allows external connections on port 5432
- Users can successfully connect remotely to PostgreSQL

 
## 4. Database Setup
- Create a database using the same name as your Linux username
- Create a schema called staging
- Generate sample data of your choice (any dataset you prefer)
- Upload/insert the data into the staging schema in your database

### STEP 1: Accessing the remote server
- To access the remote server we use the command ssh user@ipaddress and then you enter the password for the remote server like in the case below.
  
<img width="1366" height="768" alt="Screenshot (2)" src="https://github.com/user-attachments/assets/971d24ab-a358-4503-a133-dd935cbee545" />

### STEP 2
- The sudo apt update command refreshes the local database of available software packages and their latest versions, allowing your system to know exactly which updates, security patches, and new applications are available to install.
<img width="1366" height="768" alt="Screenshot (3)" src="https://github.com/user-attachments/assets/847f9470-7147-49b0-a262-957b4c04c448" />

### STEP 3: Postgresql
- Use command psql --version to check if the postgresql is installed if not use sudo apt install postgresql postgresql -contrib -y
- postgresql installs the database server.
- postgresql-contrib installs extra useful PostgreSQL tools and extensions
- Primary PostgreSQL Service Controls
  - Start service:sudo systemctl start postgresql
  - Stop service: sudo systemctl stop postgresql
  - Restart service: sudo systemctl restart postgresql
  - Reload configuration: sudo systemctl reload postgresql (Applies settings changes without closing active database connections)
  
<img width="1366" height="768" alt="Screenshot (4)" src="https://github.com/user-attachments/assets/aaf92998-c12b-474a-82d6-a30999927c30" />
<img width="1366" height="768" alt="Screenshot (5)" src="https://github.com/user-attachments/assets/8b644136-0925-4df3-b42b-ceac0db1bea9" />

### STEP 4: Add User
- To add user we use the command sudo adduser lamecko
- Point to note is that all the installations should be done under the user created and not in the superuser(which I used).
- To check how to do use users and not the main user check this link https://dev.to/david_mwandairo_777f888b4/linux-fundamentals-for-data-engineering-1hii
  
<img width="1366" height="768" alt="Screenshot (6)" src="https://github.com/user-attachments/assets/15ad2958-7cd0-474a-9e5c-80dde7f8c716" />

### STEP 5 : Postgresql Interractive mode
- First you ensure that the status of postgresql is started and active using the command sudo systemctl status postgresql.
- If it is active and running we can make postgresql interractive using command sudo -i -u postgresql
<img width="1366" height="768" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/8cc5091e-53b8-42c0-b880-83f60e44c5b3" />
<img width="1366" height="768" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/59922135-d0f4-41f6-8d45-6e4ccf3ca589" />

### STEP 6: CREATING DATABASE
- Inside the interractive mode we can create database using the commands below
- CREATE DATABASE lamecko;
- CREATE USER lamecko WITH PASSWORD '1234';

You can use these administrative shortcuts must be run inside the interactive psql shell and always begin with a backslash (\). 
- \l: List all databases.
- \c database_name: Connect to a different database.
- \dt: List all tables in the current database.
- \d table_name: Describe a table schema (columns, data types, and keys).
- \du: List all database users and their roles.
- \conninfo: Display current connection details (user, host, port).
- \?: Open the help menu for meta-commands.
- \q: Exit the psql console.

<img width="1366" height="768" alt="Screenshot (10)" src="https://github.com/user-attachments/assets/df047098-3c8f-458d-9972-a5d65b8bf8b5" />

### Enabling External Connection
- To enable external connection of our database for example to dbeaver we need to manipulate certain files in postgresql that is postgres.conf and ph-hba
- Inside postgres.conf we search for the listening address and change the localhost to (*) to enable connection to the database.
- And adding  "host    all             all             0.0.0.0/0               md5" at the bottom inside the ph-hba file
<img width="1366" height="768" alt="Screenshot (11)" src="https://github.com/user-attachments/assets/b1c56205-384e-4379-bc1b-5936ee91ebe6" />

### STEP 7 : Accessing the database in Dbeaver
- I created a new connection for postgresql, host was ip address, port 5432, database lamecko, password 1234, Tested connection and finished the connection as below.
<img width="1366" height="768" alt="Screenshot (12)" src="https://github.com/user-attachments/assets/a4751a33-3e01-48db-943c-914a1b49ad62" />


<img width="1366" height="768" alt="Screenshot (13)" src="https://github.com/user-attachments/assets/f3896dbd-e0bb-41ac-95f3-31345e28b202" />
<img width="1366" height="768" alt="Screenshot (14)" src="https://github.com/user-attachments/assets/a7d506cc-a78a-43ce-8d47-ac6998f96ebd" />













