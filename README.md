
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
<img width="1366" height="768" alt="Screenshot (3)" src="https://github.com/user-attachments/assets/847f9470-7147-49b0-a262-957b4c04c448" />
<img width="1366" height="768" alt="Screenshot (4)" src="https://github.com/user-attachments/assets/aaf92998-c12b-474a-82d6-a30999927c30" />
<img width="1366" height="768" alt="Screenshot (5)" src="https://github.com/user-attachments/assets/8b644136-0925-4df3-b42b-ceac0db1bea9" />
<img width="1366" height="768" alt="Screenshot (6)" src="https://github.com/user-attachments/assets/15ad2958-7cd0-474a-9e5c-80dde7f8c716" />
<img width="1366" height="768" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/8cc5091e-53b8-42c0-b880-83f60e44c5b3" />
<img width="1366" height="768" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/59922135-d0f4-41f6-8d45-6e4ccf3ca589" />
<img width="1366" height="768" alt="Screenshot (10)" src="https://github.com/user-attachments/assets/df047098-3c8f-458d-9972-a5d65b8bf8b5" />
<img width="1366" height="768" alt="Screenshot (11)" src="https://github.com/user-attachments/assets/b1c56205-384e-4379-bc1b-5936ee91ebe6" />
<img width="1366" height="768" alt="Screenshot (12)" src="https://github.com/user-attachments/assets/a4751a33-3e01-48db-943c-914a1b49ad62" />


<img width="1366" height="768" alt="Screenshot (13)" src="https://github.com/user-attachments/assets/f3896dbd-e0bb-41ac-95f3-31345e28b202" />
<img width="1366" height="768" alt="Screenshot (14)" src="https://github.com/user-attachments/assets/a7d506cc-a78a-43ce-8d47-ac6998f96ebd" />













