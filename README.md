# Building a Relational Database on AWS with MySQL Workbench
Creating a Relational Database on AWS (Prepared for QuickSight Visualization)

# Relational Database and Visualization with Amazon QuickSight (Prepared for QuickSight Visualization)

### 🧰 Tools Used
- **Amazon RDS**
- **MySQL Workbench**
- **Amazon QuickSight**
- **AWS IAM & Security Groups**

## 📌 Project Overview
## 📘 Project Overview

In today's project, I created a relational database on AWS using Amazon RDS and prepared it for future integration with Amazon QuickSight.  
The objective was to gain hands-on experience with setting up a cloud-based database, configuring access using IAM and security groups, and preparing structured data for visualization.

To interact with the database, I used **MySQL Workbench** to:
- Connect to the RDS instance
- Write and execute SQL queries
- Create schemas and tables
- Populate the tables with sample data

Although the QuickSight visualization step could not be completed due to access limitations, this project provided valuable practical experience with cloud infrastructure and data workflows.

## ✅ Step 1: Creating an IAM User

To ensure secure access to AWS services, I started by creating an **IAM (Identity and Access Management) user**. This IAM user is configured with the necessary permissions to access and interact with services such as Amazon RDS (for the relational database) and Amazon QuickSight (for visualization).

🔒 The IAM user enhances security by:
- Avoiding use of root credentials
- Applying **least privilege access**
- Enabling secure and trackable access through IAM policies

![IAM access success ](https://github.com/user-attachments/assets/1e8fc780-367f-4b53-a020-43aac9c2c42a)

✔️ **Outcome:** Successfully created and configured the IAM user with appropriate permissions for database and analytics tasks.

## ✅ Step 2: Creating a Database

In this step, I am creating a relational database in AWS so that I can store my data for visualization.
I am choosing **MySQL** as the database engine and selecting the **AWS Free Tier** option.  
This allows me to explore Amazon RDS features without incurring costs.

![creating data base](https://github.com/user-attachments/assets/d7a5c2d6-9a92-4556-87d1-e83130ca9bb1)

The difference between MySQL and SQL is: SQL is a query language for extracting data from a database, MySQL is a framework for setting up a database, and it's widely considered classic.

## ✅ Step 3: Connecting MySQL Workbench to RDS
In this step, I am connecting **MySQL Workbench** with my **RDS instance**.  
To do this, I need to allow access to the RDS instance by modifying the **security group** it belongs to.  
This ensures that my local machine can connect to the database securely.


I downloaded **MySQL Workbench** from the official MySQL website to use it as a visual tool for connecting to and managing my database.

The first thing I did was make my RDS instance public because I needed to connect to it from MySQL Workbench.

![security map](https://github.com/user-attachments/assets/3079bfc7-4ad0-4f6f-a422-643dae8eed35)

To allow MySQL Workbench to connect to my RDS instance, I edited the **inbound rules** of the associated security group.

- I added a rule to allow **All TCP** traffic from **My IP address**.
- This ensures that only my machine has access to the database, maintaining a secure setup.

![chnage setting inbound rules](https://github.com/user-attachments/assets/caf301a1-f00c-4316-be45-e632daabe2c7)
![security group](https://github.com/user-attachments/assets/6e2cc46b-6851-4732-a865-95e90fa878e9)

I updated the default security group for my RDS instance because security groups control what kind of traffic can access AWS resources.  
To enable a secure connection from my computer, I added **my IP address** as an accepted inbound rule.

## ✅ Step 4: Setting Up MySQL Workbench to Connect with RDS

I configured MySQL Workbench to connect to my RDS instance by entering:

- The **RDS endpoint** as the hostname  
- Port: **3306**  
- Username: **admin**  
- Password: stored securely
![trying to setup the local my sql](https://github.com/user-attachments/assets/30affae7-8763-4e10-bd7f-1e9c3f2b9e58)

This setup allowed me to access my AWS-hosted relational database directly from my local system.

In this step, I am going to create my overarching schema, add some tables, and then insert my data into the database.

## ✅ Step 5: Creating the Schema

To populate my database, I used SQL queries in the **MySQL Workbench** application to create and insert data into my tables.  
Before that, I connected MySQL Workbench to my **RDS instance** using the **endpoint, port, username, and password**.

I created a new schema named **QuickSightDatabase** in MySQL Workbench.  
This schema will be used to organize and store the tables and data for my project.

![my sql schema](https://github.com/user-attachments/assets/e24be57f-e590-4b23-98aa-6646cd22112e)

I inserted employee records into the `newhire` table using multiple `INSERT INTO` SQL statements.  
Then, I ran a `SELECT * FROM newhire;` query to confirm that the data was added correctly.

![populatig data to schema](https://github.com/user-attachments/assets/b0229d2c-4eb5-4538-aed6-3b4c2b9411af)

✔️ The data is now stored and ready to be visualized using Amazon QuickSight.

## ✅ Step 6: Connecting RDS to QuickSight

In this step, I am going to connect my **RDS instance** to **Amazon QuickSight**.  

To do this, I first need to update the **security group** for the RDS instance to allow inbound access from QuickSight.
In this step, I set up my **Amazon QuickSight** account.  
I chose the **Standard edition**, selected the **same AWS region** as my RDS instance, and clicked **"Let's get started"** to begin using QuickSight.

## ✅ Final Notes

This project gave me valuable hands-on experience with AWS and cloud-based data workflows.  
I successfully:

- Created and configured a relational database using Amazon RDS
- Set up IAM roles and updated security group settings
- Connected MySQL Workbench to RDS and populated tables using SQL
- Prepared my environment for visualization using Amazon QuickSight

While I encountered a permissions issue when connecting QuickSight to RDS, the overall process helped me better understand cloud networking, access control, and data infrastructure setup.

🔜 In future updates, I plan to:
- Finalize QuickSight connectivity
- Create visual dashboards based on my database
- Automate data loading and visualization workflows

- ## 📌 Key Takeaways

- Learned how to launch and configure an Amazon RDS instance
- Understood the role of IAM and security groups in controlling cloud resource access
- Practiced writing SQL to create tables and insert data using MySQL Workbench
- Gained experience in troubleshooting real-world permission and connectivity issues
- Prepared the environment for future integration with Amazon QuickSight
- Developed a solid understanding of cloud database setup and data visualization pipelines




This was a great learning experience and a strong step toward mastering AWS data services and business intelligence tools.




