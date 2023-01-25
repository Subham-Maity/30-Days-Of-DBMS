# [Website View](https://code-xam.vercel.app/docs/dbms/dbms2)


## ⭐ Explain Abstraction



let's say you're using a program called Tally to help you with your business. You don't need to know how Tally does all the math and accounting behind the scenes, you just need to know how to use it to make invoices and record payments. This is like abstraction, where you're only focusing on the important things you need to know to use Tally, and not worrying about the rest.


<p align="center">
            <img style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}}
                 src="https://media.giphy.com/media/EpfccjWvxn1ca5hTWZ/giphy.gif"
                 src="https://media.giphy.com/media/EpfccjWvxn1ca5hTWZ/giphy.gif"
                 width="450"/>
</p>

Another example is when you're driving a car, you don't need to know how the engine, transmission, and brakes work in order to drive the car. You just need to know how to use the gas pedal, steering wheel, and brakes to drive it. This is like abstraction too, where you're only focusing on the important things you need to know to drive the car, and not worrying about the rest.

So what is Abstraction </span>😥❓</h12>
 
Abstraction is the process of hiding the internal details of an application from the outer world. Abstraction is used to describe things in simple terms. It's used to create a boundary between the application and the client programs.




## ⭐ Goal of DBMS Abstraction


Explain with Example

<p align="center">
            <img style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}}
                 src="https://media.giphy.com/media/4TgADFrAKzq2wKyomS/giphy-downsized-large.gif"
                 width="450"/>
</p>

Let's say we have an e-commerce website called "MegaMart" that sells a wide variety of products. The website has different teams such as the logistics team, customer service team, and many more. However, not all teams have access to all the data stored on the website.


<PhotoView align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/02.%20DBMS%20Architecture/img/1.png?raw=true" alt="example">
                    <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/02.%20DBMS%20Architecture/img/1.png?raw=true" alt="example" />
                </PhotoView>
            </PhotoProvider>



  For example, the logistics team only has access to customer addresses for delivery purposes. They do not have access to customer comments or feedback. This is because the comments and feedback are used by the customer service team to improve the overall customer experience and should not be accessed by the logistics team.

Similarly, the customer service team only has access to customer comments, feedback and phone numbers for customer support. They do not have access to customer addresses as that is the responsibility of the logistics team.

 By implementing a DBMS (Database Management System) abstraction, the website can control access to the data and ensure that the correct teams have access to the information they need to perform their specific tasks. This improves the security and efficiency of the website, as well as protects the privacy of the customers.


The major purpose of DBMS is to provide users with an abstract view of the data. That is, the system hides certain details of how the data is stored and maintained.


## ⭐ 1. View of Data



Three Schema Architecture (View Of Data)

What is Schema</span>😥❓</h12>

In a database management system (DBMS), a schema is a blueprint or structure for how data is organized and stored. It defines the tables, columns, and relationships between them, as well as the rules and constraints that govern the data.

Think of a schema like a plan or a design for a house. Just like how the plan of a house shows the layout of the rooms, the location of the doors and windows, the schema of a database shows the layout of the tables, the columns and their types, and the relationship between them.

A database can have multiple schemas, each with its own set of tables and relationships. This allows for different user groups to have their own unique views of the data while still maintaining a consistent overall structure.


To simplify user interaction with the system, abstraction is applied through several levels of abstraction.

The main objective of three level architecture is to enable multiple users to access the same data with a personalized view while storing the underlying data only once in the database.

The three levels of the architecture are: external level, conceptual level, and internal level.


<PhotoView align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/02.%20DBMS%20Architecture/img/2.png?raw=true" alt="example">
                    <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/02.%20DBMS%20Architecture/img/2.png?raw=true" alt="example" />
                </PhotoView>
            </PhotoProvider>



<PhotoView align="center"  src="https://miro.medium.com/max/1100/1*Mld5pLhDxJcI_WYx1jab9w.webp" alt="example">
                    <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://miro.medium.com/max/1100/1*Mld5pLhDxJcI_WYx1jab9w.webp" alt="example" />
                </PhotoView>
            </PhotoProvider>
    


### ℹ️ Physical Level/ Internal Level:

The physical level, also known as the internal level, is the lowest level of abstraction in a database management system (DBMS). It describes how the data is actually stored on the physical storage media, such as hard drives or solid-state drives.

At this level, the DBMS uses low-level data structures, such as files, blocks, and pages, to organize and store the data. These data structures are used to optimize the performance of the database, such as by reducing disk I/O and minimizing the amount of data that needs to be read or written.

For example, in a database for a retail store, at the physical level, the data is stored in a specific format, like binary or binary large object (BLOB) format. The DBMS uses specific data structures such as B-tree, Hash tree, etc to store the data in a way that allows for efficient access and retrieval. This can include storage allocation, data compression, and encryption to protect the data.

The goal of the physical level is to define algorithms and techniques that allow efficient access to data, while minimizing the use of resources such as disk I/O and memory. This is accomplished by using techniques such as indexing, caching, and data partitioning, which can greatly improve the performance of the database.


In summary, The physical level/ internal level is the lowest level of abstraction in a DBMS, it describes how data is stored on a physical storage device such as a hard drive or solid-state drive.

**Goal:** We must define algorithms that allow efficient access to data.


### ℹ️ Logical level / Conceptual level:

eCommerce website's database:
|**Order ID**|**Customer ID**|**Product ID**|**Quantity**|**Order Date**|**Price**|
|:---:|:---:|:---:|:---:|:---:|:---:|
|1|1|1|1|2020-01-01|100|
|2|1|2|2|2020-01-02|200|
|3|2|3|3|2020-01-03|300|
|4|2|4|4|2020-01-04|400|
|5|3|5|5|2020-01-05|500|

This table represents information about orders made on the eCommerce website. Each row in the table represents a single order and contains information about that order such as the Order ID, Customer ID, Product ID, Quantity and Price.

The Order ID is a unique identifier for each order, the Customer ID and Product ID are the foreign keys that link to the customers and products table respectively. Quantity and Price are the quantity of the product purchased and the total price of the order

The table also describes relationships between the data. For example, the Customer ID and Product ID columns have a one-to-many relationship with the customers and products table respectively, meaning that a single customer can have multiple orders and a single product can be included in multiple orders.

Users interacting with this table at the logical level don't need to know about the physical level. They can simply look at the table and understand the relationships between the different pieces of information. However, the person responsible for maintaining the database (the DBA) would need to know about the physical level in order to ensure that the table is stored and organized efficiently on a computer or server.


In summary,
    - The conceptual schema describes the design of a database at the conceptual level,
    describes what data are stored in DB, and what relationships exist among those data.
    - User at logical level does not need to be aware about physical-level structures.
    - DBA, who must decide what information to keep in the DB use the logical level of
    abstraction.

**Goal:** ease to use.



### ℹ️ External level / View level:


The customer can see products, prices, and reviews, but cannot see the inventory levels or financial information. The administrator can see all the information in the database, including inventory levels and financial information.

For example, a customer logs into the eCommerce site and sees a list of products, their prices, and customer reviews. They can also add items to their cart and complete a purchase. This is the customer's view of the database.

On the other hand, an administrator logs into the site and sees the same list of products, but also has access to the inventory levels and financial information. They can also add, remove or update products, shipping details, and payment methods. This is the administrator's view of the database.

In this way, the database is separated into different schemas, or views, to simplify the user's interaction with the system and provide a security mechanism to prevent unauthorized access to certain parts of the database.




In summary,
1. Highest level of abstraction aims to simplify users' interaction with the system by
                providing different view to different end-user
2. Each view schema describes the database part that a particular user group is interested
                and hides the remaining database from that user group.
3. At the external level, a database contains several schemas that sometimes called as
                sub-schema. The sub-schema is used to describe the different view of the database.
4. At views also provide a security mechanism to prevent users from accessing certain parts
                of DB.

**Goal:** Simplify user interaction with the system.

## ⭐ 2. Instances and Schemas



Instances and Schemas


A student database may have the following schema:

|**Field**|**Data Type**|
|:---:|:---:|
|Student ID|Integer|
|First Name|String|
|Last Name|String|
|Major|String|
|GPA|Float|
|Graduation Year|Integer|
|Email|String|
|Phone Number|String|
|Address|String|
|Date of Birth|Date|
|Gender|String|
|Class Standing|String|
|Enrollment Status|String|
|Enrollment Date|Date|
|Graduation Date|Date|
|Advisor ID|Integer|

⚡ An example of a student database instance could be:</h12>



<table>
<thead>
<tr>
<th style="text-align:center"><strong>Student ID</strong></th>
<th style="text-align:center"><strong>First Name</strong></th>
<th><strong>Last Name</strong></th>
<th style="text-align:center"><strong>Major</strong></th>
<th style="text-align:center"><strong>GPA</strong></th>
<th><strong>Graduation Year</strong></th>
<th style="text-align:center"><strong>Email</strong></th>
<th style="text-align:center"><strong>Phone Number</strong></th>
<th><strong>Address</strong></th>
<th style="text-align:center"><strong>Date of Birth</strong></th>
<th style="text-align:center"><strong>Gender</strong></th>
<th><strong>Class Standing</strong></th>
<th style="text-align:center"><strong>Enrollment Status</strong></th>
<th style="text-align:center"><strong>Enrollment Date</strong></th>
<th><strong>Graduation Date</strong></th>
<th style="text-align:center"><strong>Advisor ID</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:center">12345</td>
<td style="text-align:center">John</td>
<td>Doe</td>
<td style="text-align:center">Computer Science</td>
<td style="text-align:center">3.5</td>
<td>2024</td>
<td style="text-align:center">johndoe@example.com</td>
<td style="text-align:center">555-555-5555</td>
<td>123 Main St, Anytown USA</td>
<td style="text-align:center">01/01/2000</td>
<td style="text-align:center">M</td>
<td>Junior</td>
<td style="text-align:center">Full-time</td>
<td style="text-align:center">01/01/2022</td>
<td>05/01/2024</td>
<td style="text-align:center">54321</td>
</tr>
<tr>
<td style="text-align:center">67890</td>
<td style="text-align:center">Jane</td>
<td>Smith</td>
<td style="text-align:center">Biology</td>
<td style="text-align:center">3.2</td>
<td>2023</td>
<td style="text-align:center">janesmith@example.com</td>
<td style="text-align:center">555-555-5555</td>
<td>456 Park Ave, Anytown USA</td>
<td style="text-align:center">02/02/1999</td>
<td style="text-align:center">F</td>
<td>Senior</td>
<td style="text-align:center">Full-time</td>
<td style="text-align:center">01/01/2019</td>
<td>12/01/2022</td>
<td style="text-align:center">56789</td>
</tr>
<tr>
<td style="text-align:center">11111</td>
<td style="text-align:center">Bob</td>
<td>Johnson</td>
<td style="text-align:center">Mathematics</td>
<td style="text-align:center">3.7</td>
<td>2022</td>
<td style="text-align:center">bobjohnson@example.com</td>
<td style="text-align:center">555-555-5555</td>
<td>789 Elm St, Anytown USA</td>
<td style="text-align:center">03/03/1998</td>
<td style="text-align:center">M</td>
<td>Senior</td>
<td style="text-align:center">Part-time</td>
<td style="text-align:center">01/01/2021</td>
<td>05/01/2022</td>
<td style="text-align:center">98765</td>
</tr>
<tr>
<td style="text-align:center">22222</td>
<td style="text-align:center">Samantha</td>
<td>Williams</td>
<td style="text-align:center">Chemistry</td>
<td style="text-align:center">3.3</td>
<td>2024</td>
<td style="text-align:center">samanthawilliams@example.com</td>
<td style="text-align:center">555-555-5555</td>
<td>321 Oak St, Anytown USA</td>
<td style="text-align:center">04/04/1997</td>
<td style="text-align:center">F</td>
<td>Junior</td>
<td style="text-align:center">Full-time</td>
<td style="text-align:center">01/01/2022</td>
<td>05/01/2024</td>
<td style="text-align:center">54321</td>
</tr>
<tr>
<td style="text-align:center">33333</td>
<td style="text-align:center">Michael</td>
<td>Brown</td>
<td style="text-align:center">Political Science</td>
<td style="text-align:center">3.0</td>
<td>2023</td>
<td style="text-align:center">michaelbrown@example.com</td>
<td style="text-align:center">555-555-5555</td>
<td>159 Pine St, Anytown USA</td>
<td style="text-align:center">05/05/1996</td>
<td style="text-align:center">M</td>
<td>Senior</td>
<td style="text-align:center">Full-time</td>
<td style="text-align:center">01/01/2019</td>
<td>12/01/2022</td>
<td style="text-align:center">56789</td>
</tr>
<tr>
<td style="text-align:center">44444</td>
<td style="text-align:center">Ashley</td>
<td>Moore</td>
<td style="text-align:center">Business</td>
<td style="text-align:center">3.5</td>
<td>2022</td>
<td style="text-align:center">ashleymoore@example.com</td>
<td style="text-align:center">555-555-5555</td>
<td>753 Birch St, Anytown USA</td>
<td style="text-align:center">06/06/1995</td>
<td style="text-align:center">F</td>
<td>Senior</td>
<td style="text-align:center">Part-time</td>
<td style="text-align:center">01/01/2021</td>
<td>05/01/2022</td>
<td style="text-align:center">98765</td>
</tr>
<tr>
<td style="text-align:center">55555</td>
<td style="text-align:center">David</td>
<td>Taylor</td>
<td style="text-align:center">Engineering</td>
<td style="text-align:center">3.9</td>
<td>2024</td>
<td style="text-align:center">davidtaylor@example.com</td>
<td style="text-align:center">555-555-5555</td>
<td>964 Maple St, Anytown USA</td>
<td style="text-align:center">07/07/1994</td>
<td style="text-align:center">M</td>
<td>Junior</td>
<td style="text-align:center">Full-time</td>
<td style="text-align:center">01/01/2022</td>
<td>05/01/2024</td>
<td style="text-align:center">54321</td>
</tr>
<tr>
<td style="text-align:center">77777</td>
<td style="text-align:center">Jessica</td>
<td>Anderson</td>
<td style="text-align:center">Communications</td>
<td style="text-align:center">3.6</td>
<td>2023</td>
<td style="text-align:center">jessicaanderson@example.com</td>
<td style="text-align:center">555-555-5555</td>
<td>111 Cedar St, Anytown USA</td>
<td style="text-align:center">08/08/1993</td>
<td style="text-align:center">F</td>
<td>Senior</td>
<td style="text-align:center">Full-time</td>
<td style="text-align:center">01/01/2019</td>
<td>12/01/2022</td>
<td style="text-align:center">56789</td>
</tr>
</tbody>
</table>


In this example, the schema defines the structure of the database, including the field names and data types. The instance represents the actual data stored in the database at a particular moment in time. The schema is the overall design of the database and does not change frequently, while the instance may change frequently as new students are added or existing student information is updated.

A database schema is the overall design of the database, including the field names and data types. The physical schema refers to how the data is stored in the database, while the logical schema refers to how the data is organized and viewed by users and application programs. Logical schema is more important for application programs and it can change without affecting the physical schema or application programs, which is known as physical data independence.



- The collection of information stored in the DB at a particular moment is called an instance of DB.
-  The overall design of the DB is called the DB schema.
- Schema is structural description of data. Schema doesn't change frequently. Data may change
 frequently.
- DB schema corresponds to the variable declarations (along with type) in a program.
- We have 3 types of Schemas: Physical, Logical, several view schemas called subschemas
- Logical schema is most important in terms of its effect on application programs, as programmers
        construct apps by using logical schema.
 - Physical data independence, physical schema change should not affect logical
        schema/application programs.



## ⭐ 3. Data Models:



Example of a Data Model


A data model is a conceptual tool that is used to describe the design of a database at a logical level. It provides a way to organize and structure data, as well as define relationships, semantics, and consistency constraints.


<table>
<thead>
<tr>
<th style="text-align:left"><strong>Data Model</strong></th>
<th style="text-align:left"><strong>Description</strong></th>
<th style="text-align:left"><strong>Example</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">Entity-relationship (ER) model</td>
<td style="text-align:left">A graphical representation used to describe the structure of a database. It is composed of entities and relationships.</td>
<td style="text-align:left">A database for a retail store that has entities such as customers, orders, and products, and relationships such as a customer placing an order and an order containing multiple products.</td>
</tr>
<tr>
<td style="text-align:left">Relational Model</td>
<td style="text-align:left">A tabular representation of data where each table represents a specific entity and the columns represent the attributes of that entity.</td>
<td style="text-align:left">A database for a retail store that has a table called &quot;customers&quot; with columns for &quot;customer_id&quot;, &quot;name&quot;, &quot;address&quot;, and &quot;phone_number&quot;, and each row represents a different customer.</td>
</tr>
<tr>
<td style="text-align:left">Object-oriented data model</td>
<td style="text-align:left">A data model that uses classes and objects to represent data and the relationships between them.Similar to the object-oriented programming paradigm.</td>
<td style="text-align:left">A database for a university that has classes such as students, courses, and professors, and the relationships between them are defined through the use of inheritance and associations.</td>
</tr>
<tr>
<td style="text-align:left">Object-relational data model</td>
<td style="text-align:left">A data model that combines the features of both object-oriented and relational data models. It provides the user with the ability to model the data in both an object-oriented and a relational way.</td>
<td style="text-align:left">A database for a bank that has objects such as accounts, transactions, and customers, and relationships between them are defined through the use of complex data types, such as object types, and user-defined types.</td>
</tr>
</tbody>
</table>




Data Models:

- Provides a way to describe the design of a DB at logical level.
- Underlying the structure of the DB is the Data Model; a collection of conceptual tools for describing
            data, data relationships, data semantics & consistency constraints.
- E.g, ER model, Relational Model, object-oriented model, object-relational data model etc.





## ⭐ 4. Database Languages:



Explain the Database Languages


Database languages are used to interact with a database and perform different types of operations on it. There are two main types of database languages: Data definition language (DDL) and Data manipulation language (DML).

- DDL is used to specify the database schema. It is used to create, alter, and delete database objects such as tables, indexes, and views. For example, in SQL, the CREATE TABLE statement is used to create a new table, and the ALTER TABLE statement is used to modify an existing table.

- DML is used to express database queries and updates. It is used to insert, update, and delete data in the database. DML also includes a query language, which is used to retrieve information from the database. For example, in SQL, the SELECT statement is used to retrieve data from a table, the INSERT statement is used to insert new data into a table, and the UPDATE statement is used to modify existing data in a table.

Both DDL and DML are present in most DB languages, like SQL. For example, in SQL, the CREATE TABLE statement is used to create a new table, which is a DDL statement, and the SELECT statement is used to retrieve data from a table, which is a DML statement.

DDL's consistency constraints are checked every time a DB is updated. For example, a constraint could be that a certain column must contain a unique value for each row in a table.

DML's data manipulation involves retrieval, insertion, deletion and updating of information stored in DB. For example, in SQL, the SELECT statement is used to retrieve data from a table, the INSERT statement is used to insert new data into a table, the DELETE statement is used to delete data from a table, and the UPDATE statement is used to modify existing data in a table.

To summarise, database languages are used to interact with a database and perform different types of operations on it. DDL is used to specify the database schema, DML is used to express database queries and updates and it includes a query language which is used to retrieve information from the database.



- Data definition language (DDL) to specify the database schema.
- Data manipulation language (DML) to express database queries and updates.
- Practically, both language features are present in a single DB language, e.g. SQL language,
- DDL
       i) We specify consistency constraints, which must be checked, every time DB is updated.

- DML

i) Data manipulation involves

1. Retrieval of information stored in DB.


2. Insertion of new information into DB.


3. Deletion of information from the DB,


4. Updating existing information stored in DB.
                
ii) Query language, a part of DML to specify statement requesting the retrieval of information.




## ⭐ 5. Application programs



How is Database accessed from Application programs


In order for an application program to access a database, it needs to use a database management system (DBMS) API. An API (Application Programming Interface) is a set of routines, protocols, and tools for building software and applications.

For example, a banking system's module generating payrolls may need to access a database in order to retrieve employee information. The application program, which is written in a host language such as C/C++ or Java, would use the appropriate API to send data manipulation language (DML) statements (e.g., SELECT, INSERT, UPDATE, DELETE) to the database. The API would then take care of sending the statements to the DBMS, which would execute them and return the results to the application program.

Two common APIs used to access databases from application programs are Open Database Connectivity (ODBC) and Java Database Connectivity (JDBC). ODBC is a Microsoft API that allows programs written in C/C++ to access a variety of databases, while JDBC is a Java API that allows Java programs to access databases. Both APIs provide a set of functions and methods that can be used to connect to a database, send SQL statements, and retrieve results.

- Apps (written in host languages, C/C++, Java) interacts with DB.
- E.g., Banking system's module generating payrolls access DB by executing DML statements from the host language.
- API is provided to send DML/DDL statements to DB and retrieve the results.

   i. Open Database Connectivity (ODBC), Microsoft "C.

   ii. Java Database Connectivity (JDBC), Java.



## ⭐ 6. Database Administrator



Database Administrator (DBA)


A Database Administrator (DBA) is a person responsible for the overall management and performance of a database or a group of databases. They have central control over both the data and the programs that access the data. They are responsible for ensuring the availability, performance, and security of the database.

An example of a DBA in the real world could be someone who works for a large retail company. This person would be responsible for managing the company's databases that store information such as customer data, sales data, and inventory data. They would be responsible for tasks such as:

1. Schema Definition: creating and maintaining the structure of the databases, including table and field definitions.
2. Storage structure and access methods: determining how the data should be stored and optimized for quick retrieval.
3. Schema and physical organization modifications: making changes to the database structure as needed.
4. Authorization control: managing user access to the databases and ensuring that only authorized individuals have access to sensitive data.
5. Routine maintenance: performing regular tasks such as backups and security patches to ensure the integrity and availability of the data.
6. Any upgrades: Upgrading the database software as per the requirement and compatibility.

This DBA would work closely with the company's IT department and other teams to ensure that the databases are running smoothly and that the data is accurate and accessible. They would also be responsible for troubleshooting any issues that may arise with the databases and ensuring that the data is protected from unauthorized access or breaches.



a. A person who has central control of both the data and the programs that access those data.

b. Functions of DBA

1) Schema Definition

2) Storage structure and access methods.

3) Schema and physical organization modifications.

4) Authorization control.

5) Routine maintenance

     i. Periodic backups.

     ii. Security patches.

     iii. Any upgrades.


## ⭐ 7. Application Architectures



DBMS Application Architectures


<PhotoView align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/02.%20DBMS%20Architecture/img/6.png?raw=true" alt="example">
                    <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/02.%20DBMS%20Architecture/img/6.png?raw=true" alt="example" />
                </PhotoView>
            </PhotoProvider>
   

<h12 className ="font-bold text-2xl sm:text-4xl align-middle ml-8">T1 Architecture</h12>


T1 Architecture: Imagine you have a small store, and you keep track of your inventory using a simple database on your computer. The database, the server, and the program you use to access the database all run on the same machine. This is an example of T1 architecture.


<PhotoView align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/02.%20DBMS%20Architecture/img/3v5.png?raw=true" alt="example">
                    <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/02.%20DBMS%20Architecture/img/3v5.png?raw=true" alt="example" />
                </PhotoView>
            </PhotoProvider>
            <figcaption>
      
**Single Tier DBMS Architecture is used whenever:**

- The data isn't changed frequently.
- No multiple users are accessing the database system.
- We need a direct and simple way to modify or access the database for application development.


**Highlights:**

1- Simplest DBMS architecture.

2- All the components of DBMS, i.e., the server, database, and client, reside on a single system.

3- The user can directly access the database.

4- Used when data isn't changing frequently.

5- Suitable for programmers, database designers, and single-user access.


<h12 className ="font-bold text-2xl sm:text-4xl align-middle ml-8">T2 Architecture</h12>


T2 Architecture: Now imagine your store is growing and you want to access your inventory database from multiple computers. You set up a separate server machine to run the database and allow other computers, or clients, to connect to it and access the data through a program. This is an example of T2 architecture.


<PhotoView align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/02.%20DBMS%20Architecture/img/4.png?raw=true" alt="example">
                    <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/02.%20DBMS%20Architecture/img/4.png?raw=true" alt="example" />
                </PhotoView>
            </PhotoProvider>
      
**The main advantages of having a two-tier architecture over a single tier are:**

- Multiple users can use it at the same time. Hence, it can be used in an organization.
- It has high processing ability as the database functionality is handled by the server alone.
- Faster access to the database due to the direct connection and improved performance.
- Because of the two independent layers, it's easier to maintain.


**Note - The main disadvantages of Two-Tier DBMS Architecture are:*

- **Scalability** - As the number of clients increases, the load on the server increases. Thereby declining the performance of the DBMS and, in turn, the client-side application.

- **Security** - The Direct connection between the client and server systems makes this architecture vulnerable to attacks.

**Highlights:**

1- Similar to a client-server architecture.

2- Faster access, Easier to maintain, and can handle multiple users simultaneously.

3-Used when we wish to access DBMS via applications and APIs.

4-Has scalability and security issues because of direct client-server connection.

<h12 className ="font-bold text-2xl sm:text-4xl align-middle ml-8">T3 Architecture</h12>


T3 Architecture: As your store becomes even bigger, you decide to create a web application for customers to view and purchase items online. The web application runs on a separate server, called an application server, which communicates with the database server to retrieve and update data. The customers access the web application through their web browsers on their own computers, which act as the clients. This is an example of T3 architecture.

<PhotoView align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/02.%20DBMS%20Architecture/img/5.png?raw=true" alt="example">
                    <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/02.%20DBMS%20Architecture/img/5.png?raw=true" alt="example" />
                </PhotoView>
            </PhotoProvider>


- **Scalability** - Since the database server isn't aware of any users beyond the application layer and the application layer implements load balancing, there can be as many clients as you want.
- **Data Integrity** - Data corruption and bad requests can be avoided because of the checks performed in the application layer on each client reques.
- **Security** - The removal of the direct connection between the client and server systems via abstraction reduces unauthorized access to the database.

**Note - In Three Tier DBMS Architecture, an additional layer (Application Layer) is added between the Client and the Server. This increases the number of layers present between the DBMS and the end-users, making the implementation of the DBMS structure complex and difficult to maintain.*

**Highlights:**

1- Most widely used DBMS architecture.

2- Follows Client-Application-Server architecture.

3- Enhanced security, data integrity, and scalability.

4-Has complexity and maintenance issues because of the extra layer.

        
In summary, T1 architecture is used for small, simple databases where everything runs on one machine. T2 architecture is used for small to medium-sized databases where the client and server are on separate machines. T3 architecture is used for large-scale web applications where the client, application server and DB server are on separate machine, and the app server is the middle layer between client and DB.
        
DBMS Application Architectures: Client machines, on which remote DB users work, and server machines on which DB system runs.


a. Tl Architecture

i. The Client, server & DB all present on the same machine.

b. T2 Architecture

i. App is partitioned into 2-components.

ii. Client machine, which invokes DB system functionality at server end through query language
 statements.

iii. API standards like ODBC & JDBC are used to interact between client and server.

 c. T3 Architecture

i. App is partitioned into 3 logical components.


ii. Client machine is just a frontend and doesn't contain any direct DB calls.

iii. Client machine communicates with App server, and App server communicated with DB.
system to access data.

iv. Business logic, what action to take at that condition is in App server itself.

     v.  T3 architecture is best for WWW Applications-

vi. Advantages:

     1. Scalability due to distributed application servers.

     2. Data integrity, App server acts as a middle layer between the client and DB, which minimize the chances of data corruption.

     3. Security, the client can't directly access DB, hence it is more secure.






# [Check Here](https://code-xam.vercel.app/docs/dbms/dbms1#-quick-mcqs)
