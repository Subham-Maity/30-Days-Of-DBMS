# [Website View](https://code-xam.vercel.app/docs/dbms/dbms3)


## ⭐ What is Data Model ?

Imagine you have a small library and you want to keep track of the books you have in stock. Without a data model, you might just have a list of all the books and their information such as title, author, and number of pages. But with a data model, you can organize your data in a more structured way.

For example, you could create a relational database with two tables: one for books and one for authors. The books table would have columns for the title, number of pages, and the author's name. The authors table would have columns for the author's name and contact information.

You can set up a relationship between the two tables by linking the author's name in both tables. So, when you want to know the contact information of the author of a specific book, you can easily find it by looking up the author's name in the authors table.

Additionally, you can also set consistency constraints, such as the author's name must be in proper format, or the number of pages must be a positive number.

By using a data model, you can effectively organize your data in a way that makes it easy to understand and query, helping you to better manage your library's book collection.



<p align="center">
            <img style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}}
                 src="https://media.giphy.com/media/jakQnxhPwrbOdEZDul/giphy.gif"
                 width="450"/>
</p>

**Books Table**
| Book ID | Title         | Author       | Pages |
|---------|---------------|--------------|-------|
| 1       | "To Kill a Mockingbird"  | "Harper Lee" | 312   |
| 2       | "The Great Gatsby"       | "F. Scott Fitzgerald" | 180   |
| 3       | "The Catcher in the Rye" | "J.D. Salinger" | 277   |

**Authors Table**
| Author       | Contact Information |
|--------------|---------------------|
| "Harper Lee" | "hlee@email.com"    |
| "F. Scott Fitzgerald"  | "fsfitz@email.com" |
| "J.D. Salinger"        | "jds@email.com"    |


As you can see, the books table has columns for the book's title, author, and number of pages, while the authors table has columns for the author's name and contact information. The two tables are linked by the author's name, so you can easily retrieve the contact information of an author by looking up their name in the authors table.

The data model also helps in validating the data before inserting into the table, for example, ensuring that the author name is in proper format and number of pages is a positive number.

By using this data model, you can easily track your library's book collection, and find information about books and authors quickly and efficiently.


Data Model: Collection of conceptual tools for describing data, data relationships, data semantics, and consistency constraints.




## ⭐ ER model

Entity-Relationship (ER) model


<PhotoView  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/1.png?raw=true" alt="example">
<img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/1.png?raw=true" alt="example" />


ER (Entity-Relationship) model is a method of modeling a database that is used to represent the relationships between entities and their attributes. The ER model is composed of three main components: entities, attributes, and relationships.

The ER diagram was proposed by Peter Chen in 1971 as a visual tool to represent the ER model. He wanted to use the ER model as a conceptual modeling approach for DBMS. Let's understand this with the help of a simple example. Suppose you need to design a database for a school.


In this database, a student is an entity with attributes such as an address, name, id, age, grades, etc.


<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/2.png?raw=true" alt="example" width="300px">
                    <img align="middle" className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/2.png?raw=true" alt="example" width="300px" />
                </PhotoView>
 </PhotoProvider>



The address can be another entity with attributes like city, street name, pin code, etc and there will be a relationship between them. 


 <PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/3.png?raw=true" alt="example" width="300px">
  <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/3.png?raw=true" alt="example" width="300px" />
     </PhotoView>
</PhotoProvider>



A graphical representation of the ER model is an ER diagram, which acts as a blueprint for the database. It shows the entities, attributes, and relationships between them.

Here's a table that shows the relationship between a student, a professor, and a course:

**Books Table**
| **Student ID** | **Student Name** | **Professor ID** | **Course ID** | **Course Name** |
|---------|---------------|--------------|-------|-------|
| 1 | Subham Maity | 101 | Rajendra Singh | CSC101 | Introduction to Computer Science |
| 2 | John Doe | 102 | John Smith | CSC102 | Data Structures and Algorithms |
| 3 | Jane Doe | 103 | Jane Smith | CSC103 | Database Management Systems |
| 4 | John Smith | 104 | John Doe | CSC104 | Operating Systems |
| 5 | Jane Smith | 105 | Jane Doe | CSC105 | Computer Networks |

In this table, the entities are students, professors, and courses, and the relationships between them are represented by the foreign keys (``Professor ID and Course ID``) in the table.


ER diagram is a graphical representation of entities and their relationships in a database, used to model and design the data structure of a system. It shows the entities, attributes, and relationships between them, acting as a blueprint for the database and helping to understand and organize the data in an efficient way.





## ⭐ Component of ER Diagram


The ER diagram consists of three basic concepts:

- Entities
- Attributes
- Relationships

<img  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/4.png?raw=true"></img>
  

                




### ⚡ Entities


#### ❓ Entity



An entity is anything in the real world, such as an object, class, person, or place. Objects that physically exist and are logically constructed in the real world are called entities. Each entity consists of several characteristics or attributes that describe that entity. For example, if a person is an entity, its attributes or characteristics are age, name, height, weight, occupation, address, hobbies, and so on.



#### ❓ Entity Set


An example of an entity set is a "Student" entity set. This entity set would contain multiple entities, each representing a student. Each student entity would have attributes such as "name," "student ID," "age," "major," etc. These attributes would have similar values across all entities within the "Student" entity set, such as all students having a unique student ID and a specific age.

| Name         | Student ID | Age | Major       |
|--------------|------------|-----|-------------|
| John Smith   | 123456     | 22  | Computer Science |
| Jane Doe     | 234567     | 21  | Biology          |
| Michael Brown| 345678     | 20  | Economics        |
| Emily Johnson| 456789     | 19  | Mathematics      |

In this table, the columns represent the attributes of the entities in the "Student" entity set (name, student ID, age, and major) and the rows represent individual entities (John Smith, Jane Doe, Michael Brown, Emily Johnson). Each student has a unique student ID and a specific age, and share similar attributes, which are name, student ID, age and major.



**Entity Set:** is a group of entities of similar kinds. It can contain entities with attributes that share similar values. It's collectively a group of entities of a similar type. For example, a car entity set, an animal entity set, a bank account entity set, and so on.




#### ❓ Entity Types



An Entity is an object of a Type Entity and the set of all entities is called an entity set.


<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/5.png?raw=true" alt="example" width="300px">
        <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}}   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/5.png?raw=true" alt="example" width="300px" />
                </PhotoView>
            </PhotoProvider>
 
Entities are of two types:
##### ✅ Strong entity
**Strong entity:** A strong entity is an entity that has a primary key and does not depend on any other entity. For example, in a database of student information, a student would be a strong entity because they have a unique student ID which serves as a primary key and the student's information does not depend on any other entity.

**Note* : A strong entity is an entity type that has a key attribute and it is represented by a single rectangle in the ER diagram.


##### ✅ Weak entity
**Weak entity:** A weak entity is an entity that does not have a primary key and depends on another entity. For example, in the same database, a class that a student is enrolled in would be a weak entity because it does not have a unique ID and it depends on the student entity (i.e. a student can be enrolled in multiple classes)

**Note* : A weak entity is an entity type that does not have a key attribute therefore, a foreign key must be used in combination with its attributes to create a primary key.It relies on another powerful entity for its unique identity and it is represented by a double-outlined rectangle in the ER diagram.



<PhotoView src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/6.png?raw=true" alt="example" >
                    <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/6.png?raw=true" alt="example"  />
                </PhotoView>
            </PhotoProvider>


Employee and Department are two strong entities, thus they are represented by a single rectangle in the above image. This gives information about employees working in a specific department, so it's represented by a single diamond. In the above image, if we remove the relationship between the two entities, both will exist, i.e. Employee and Department since they are independent of one another.


**Another Example:**


<PhotoView  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/7.png?raw=true" alt="example" >
                    <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/7.png?raw=true" alt="example"  />
                </PhotoView>
            </PhotoProvider>

- A single rectangle is used to represent strong entities.
- A single diamond is used to represent the relationship between two strong entities.

| No | Property | Strong Entities | Weak Entities |
|------|----------|-----------------|---------------|
| 1    | Key      | Has a primary key | Does not have a primary key |
| 2    | Dependency | It is independent i.e its existence does not depend on other entity. | Dependent on another strong entity |
| 3    | Representation | It is represented using a single rectangle(single table) | It is represented using a double rectangle. (Represented by a separate table with a foreign key referencing the parent entity) |
| 4    | Relationship representation | A single diamond is used to represent the relationship between two strong entities. | A double diamond is used to represent the relationship between two weak entities. |
| 5    | Participation | It may or may not participate in a relationship between entities. | It always participates in the relationship between entities since its existence is dependent on other strong entities and it always has total participation. |
| 6    | Example | Student (with unique student ID as primary key) | Enrollment (depends on the student and represented by a separate table with a foreign key referencing the student ID) |



**Entity:** An Entity is a “thing” or “object” in the real world that is **distinguishable** from all other objects.
1. It has physical existence.
2. Each student in a college is an entity.
3. Entity can be uniquely identified. (By a primary attribute, aka Primary Key)
4. **Strong Entity:** Can be uniquely identified.
5. **Weak Entity:** Can’t be uniquely identified., depends on some other strong entity.
- It doesn’t have sufficient attributes, to select a uniquely identifiable attribute.
- Loan -> Strong Entity, Payment -> Weak, as instalments are sequential number counter can be generated separate for each loan.
- Weak entity depends on strong entity for existence.
5. Entity set
- It is a set of entities of the same type that share the same properties, or attributes.
- E.g., Student is an entity set.
- E.g., Customer of a bank



### ⚡ Attributes


#### ❓ Attribute


An entity is represented by a set of attributes. Each entity has a value for each of its attributes. For each attribute, there is a set of permitted values, called the domain, or value set, of that attribute.E.g., Student Entity has following attributes
A. Student_ID
B. Name
C. Standard
D. Course
E. Batch
F. Contact number
G. Address

For example, here id, Name, Age, and Mobile_No are the attributes that define the entity type Student.

<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/8.png?raw=true" alt="example" width="300px" >
                    <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/8.png?raw=true" alt="example" width="300px" />
                </PhotoView>
            </PhotoProvider>


#### ❓ Types of Attributes



Types of Attributes


There are five types of attributes:

- Simple attribute:
- Composite attribute:
- Single-valued attribute:
- Multi-valued attribute:
- Derived attribute:


##### ✅ Simple:
An attribute that cannot be further decomposed into smaller parts is called a simple attribute.E.g., Name, Age, Mobile_No, etc.

- It's an atomic value and is also known as the key attribute. The simple attributes are represented by an oval shape in ER diagrams with the attribute name underlined.
- Attributes which can’t be divided further.
- E.g., Customer’s account number in a bank, Student’s Roll number etc.

For example, the roll number of a student, or the student's contact number are examples of simple attributes.

<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/9.png?raw=true" alt="example" width="300px" >
                        <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/9.png?raw=true" alt="example" width="300px" />
                    </PhotoView>
                </PhotoProvider>


##### ✅ Composite:

An attribute that composed of many other attributes is known as a composite attribute. E.g., Address, Name, etc.
- Can be decomposed into simple attributes is known as a composite attribute.
- The composite attribute is represented by an ellipse.
- Can be divided into subpart (that is, other attributes).(It is a combination of two or more simple attributes.)
- E.g., Name of a person, can be divided into first-name, middle-name, last-name.
- If user wants to refer to an entire attribute or to only a component of the attribute.
- Address can also be divided, street, city, state, PIN code.

For example, A name can be divided into first name, middle name, and last name.

<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/10.png?raw=true" alt="example" width="300px" >
                        <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/10.png?raw=true" alt="example" width="300px" />
                    </PhotoView>
</PhotoProvider>

For example, A student's address can be divided into city, state, country, and pin code.

<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/11.png?raw=true" alt="example" width="300px" >
                        <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/11.png?raw=true" alt="example" width="300px" />
                    </PhotoView>
                </PhotoProvider>
                <figcaption>
                    Change the image size by using the click-and-scroll function.
                </figcaption>
            </figure>
        </div>

##### ✅ SingleValued:

Single valued attributes are those attributes that consist of a single value for each entity instance and can't store more than one value. The value of these single-valued attributes always remains the same, just like the name of a person.

- An attribute that can store only one value for each entity instance is called a single-valued attribute.
- The single-valued attribute is represented by a rectangle.
- E.g., Name, Age, etc.

For example, Student is an entity and the name , age, and roll number are the attributes of the student entity. The name, age, and roll number are single-valued attributes.We can't further subdivide these attributes, and hence, they are simple as well as single-valued attributes.

<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/12.png?raw=true" alt="example" width="300px" >
                        <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/12.png?raw=true" alt="example" width="300px" />
                    </PhotoView>
                </PhotoProvider>


##### ✅ MultiValued:

Multi-valued attributes are those attributes that can store more than one value for each entity instance. The value of these multi-valued attributes can change, just like the phone number of a person.

- Limit constraints may be applied and upper or lower limits may be specified.
- The multi-valued attribute is represented by a parallelogram.
- Ex. Phone number, email address, nominee-name, dependent-name, etc.


<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/13.png?raw=true" alt="example" width="300px" >
                        <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/13.png?raw=true" alt="example" width="300px" />
                    </PhotoView>
                </PhotoProvider>
    


##### ✅ Derived:

Derived attributes are those attributes whose values can be derived from the values of other attributes. They are always dependent upon other attributes for their value.
        For example, we can derive the Age attribute, which changes every year, and can easily calculate the age of a person from his/her date of birth value. Hence, the Age attribute here is derived attribute from the DOB single-valued attribute.

- They are always dependent upon other attributes for their value.
- Derived attributes are always represented by dashed or dotted elliptical shapes.
- The age attribute can be derived from the date of birth (DOB) attribute. So, it's a derived attribute.
- Value of this type of attribute can be derived from the value of other related attributes.
- Ex. Age, Loan-age, etc.


<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/14.png?raw=true" alt="example" width="300px" >
                        <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/14.png?raw=true" alt="example" width="300px" />
                    </PhotoView>
                </PhotoProvider>




 ##### ✅ Additional:
###### ❗ Complex Attributes:
Complex attributes are rarely used in DBMS. They are formed by combining two or more attributes. They are represented by a rectangle with a dotted line inside it.These attributes always have many sub-sections in their values.

- Complex attributes are rarely used in DBMS.
- They are formed by combining two or more attributes.
```sql
 Address_EmPhone({Phone}, {Email}, Address{Street, City, State, PIN code)}
 ```
<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/15.png?raw=true" alt="example"  >
                        <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/15.png?raw=true" alt="example" />
                    </PhotoView>
                </PhotoProvider>


 attribute. Email and Phone number are multi-valued attributes while Address is a composite attribute which is further subdivided as House number, Street, City & State. This combination of multi-valued and composite attributes altogether forms a complex attribute.




###### ❗ Stored Attributes:

Values of stored attributes remain constant and fixed for an entity instance and also, and they help in deriving the derived attributes. For example, the Age attribute can be derived from the Date of Birth attribute, and also, the Date of birth attribute has a fixed and constant value throughout the life of an entity. Hence, the Date of Birth attribute is a stored attribute.

- Values of stored attributes remain constant and fixed for an entity instance.
- They help in deriving the derived attributes.





<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/16.png?raw=true" alt="example"  >
                        <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/16.png?raw=true" alt="example" />
</PhotoView>




##### 🗒️ Summary:

| Attribute Type | Description | Example |
| --- | --- | --- |
| Simple | Cannot be further subdivided and are atomic | "Name" which is a simple attribute and can't be divided into any other component. |
| Composite | Composed of multiple simple attributes | "Address" which is a composite attribute and can be divided into street, city, state, and zip code. |
| Single-Valued | Can only store one value per entity instance | "Salary" which is a single-valued attribute and can only store one salary value for each entity instance |
| Multi-Valued | Can store multiple values per entity instance | "Hobbies" which is a multi-valued attribute and can store multiple hobbies for each entity instance |
| Derived | Values can be calculated from other attributes | "GPA" which is a derived attribute and can be calculated from course grades |
| Stored | Values remain constant and fixed for an entity instance | "Birthdate" which is a stored attribute and its value remains constant and fixed for each entity instance. |
| Key | Uniquely identifies an entity within an entity set | "Social Security Number" which is a key attribute and can uniquely identify an entity from an entity set |
| Complex | Combination of multi-valued and composite attributes | "Employee Profile" which is a complex attribute and can be formed by combination of multi-valued and composite attributes like Employee's multiple skills and address.|


##### 📚 Complete Diagram:

Here is the complete student diagram with all the attributes where address is the composite attribute, age is the derived attribute, phone number is the multivalued attribute, and roll number is the key attribute.


<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/17.png?raw=true" alt="example"  >
                        <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/17.png?raw=true" alt="example" />
                    </PhotoView>



##### 🚩 Extra: NULL Value


1. An attribute takes a null value when an entity does not have a value for it.
2. It may indicate “not applicable”, value doesn’t exist. e.g., person having no middle-name
3. It may indicate “unknown”.
- . Unknown can indicate missing entry, e.g., name value of a customer is NULL, means it is missing as name must have some value.
- . Not known, salary attribute value of an employee is null, means it is not known yet.

### ⚡ Relationships


A relationship is used to describe the relation between entities. Diamond or rhombus is used to represent the relationship.
- A relationship is used to describe the relation between entities.
- Diamond or rhombus is used to represent the relationship.

<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/18.png?raw=true" alt="example"  >
                        <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/18.png?raw=true" alt="example" />
                    </PhotoView>



Another Examples:

- Teacher teaches Student
- Female married to Male
- Scientist invent Invention
- Student enroll Course
- Employee is assigned Project
- Athlete plays Sport
- Manager manages Team
- Chef cooks Dish
- Writer writes Book
- Director directs Movie
- Musician performs Song
- Artist creates Artwork
- Designer designs Product
- Actor performs in Play
- Coach trains Athlete
- Driver drives Vehicle
- Mechanic repairs Car
- Parent raises Child
- Author writes Article
- Programmer codes Software
- Sailor navigates Ship
- Engineer builds Structure



#### ❓ Degree of Relationship


In DBMS, the degree of relationship is the number of entities involved in the relationship.

This is determined when designing a database by first deciding on the entities, then the relationship between them. For example, a database for a company could have entities such as employee, department, project, etc. The degree of the relationship between these entities is defined as the total number of entities involved in that relationship. This can be visualized in an E-R diagram, which shows the relationship between entities in a database's design. The E-R diagram uses symbols such as rectangles for entities, ovals for attributes, and diamonds for relationships.

There are 4 types of degrees of relationship based on the involved entities-

- Unary relationship
- Binary relationship
- Ternary relationship
- N-ary relationship

##### ✅ Unary relationship

A unary relationship is a relationship between a single entity and itself. For example, a person can be a friend of himself. In this case, the degree of the relationship is 1.

- A unary relationship is a relationship between a single entity and itself.
- For example, a person can be a friend of himself.
- In this case, the degree of the relationship is 1.
- The unary relationship is also known as a recursive relationship.


<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/19.1.png?raw=true" alt="example"  >
                        <img  className="bg-purple-900 dark:bg-stone-900" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/19.1.png?raw=true" alt="example" />
                    </PhotoView>

##### ✅ Binary relationship

A binary relationship is a relationship between two entities. For example, a person can be a friend of another person. In this case, the degree of the relationship is 2.

- A binary relationship is a relationship between two entities.
- In this case, the degree of the relationship is 2.
- Example- Each Indian citizen has their own Aadhar Card so we can say that citizen and Aadhar Card are two entities involved.




<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/20.png?raw=true" alt="example"  >
                        <img  className="bg-purple-900 dark:bg-stone-900"  align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/20.png?raw=true" alt="example" />
                    </PhotoView>



##### ✅ Ternary relationship

A ternary relationship is a relationship between three entities. For example, a person can be a friend of another person and that person can be a friend of another person. In this case, the degree of the relationship is 3.

- A ternary relationship is a relationship between three entities.
- In this case, the degree of the relationship is 3.
- Example- A student can enroll in multiple courses and a course can have multiple students enrolled in it. So, we can say that student, course, and enrollment are three entities involved.
- Another Example- A student studies in a school, so student and school are two entities. But, the same student also takes some coaching classes, so he has a relation with coaching as well, so coaching class is also an entity. Here as there are 3 entities, so it is a ternary relationship.


<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/21.png?raw=true" alt="example"  >
                        <img  className="bg-purple-900 dark:bg-stone-900"  align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/21.png?raw=true" alt="example" />
                    </PhotoView>


##### ✅ N-ary relationship

An N-ary relationship is a relationship between N entities. For example, a person can be a friend of another person and that person can be a friend of another person and so on. In this case, the degree of the relationship is N.

- An N-ary relationship is a relationship between N entities.
- In this case, the degree of the relationship is N.
- Example- A student can enroll in multiple courses and a course can have multiple students enrolled in it. So, we can say that student, course, and enrollment are three entities involved.
- Another Example- Let us consider the example of a university. It has many entities like students, teachers, affiliated colleges, courses, etc. Here, there are many entities associated with the university.

<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/22.png?raw=true" alt="example"  >
                        <img  className="bg-purple-900 dark:bg-stone-900"  align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/22.png?raw=true" alt="example" />
                    </PhotoView>

#### ❓ Relationships Constraints



There are two types of constraints in a relationship.
- Mapping constraints/Cardinality constraints
- Participation constraints


##### ✅ Cardinality constraints

Cardinality constraints are the constraints that define the number of entities that can participate in a relationship. There are four types of cardinality constraints.

For the binary relationship set there are entity set A and B then the mapping cardinality can be one of the following −

- One-to-one

- One-to-many

- Many-to-one

- Many-to-many

###### ℹ️ One-to-one

In a one-to-one relationship, each entity in one entity set is related to only one entity in the other entity set. For example, a person can have only one passport and a passport can belong to only one person.

- Entity in A associates with at most one entity in B, where A & B are entity sets and an entity of B is associated with at most one entity of A.
- Ratio of entities in A to entities in B is 1:1.
- Eg- Citizen has Adhar card and Adhar card belongs to only one citizen or Female married to Male



<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/23.png?raw=true" alt="example"  >
                        <img  className="bg-purple-900 dark:bg-stone-900"  align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/23.png?raw=true" alt="example" />
                    </PhotoView>
                </PhotoProvider>

###### ℹ️ One-to-many

In a one-to-many relationship, each entity in one entity set is related to many entities in the other entity set. For example, a person can have many bank accounts and a bank account can belong to only one person.

- Entity in A associates with at most one entity in B, where A & B are entity sets and an entity of B is associed with at most one entity of A.
- Ratio of entities in A to entities in B is 1:M.
- Eg- Scientist invents many inventions and an invention is invented by only one scientist or a student can enroll in many courses and a course can have many students enrolled in it.
- Another Ex: Citizen has vahicle and vehicle belongs to only one citizen


<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/24.png?raw=true" alt="example"  >
                        <img  className="bg-purple-900 dark:bg-stone-900"  align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/24.png?raw=true" alt="example" />
                    </PhotoView>


###### ℹ️ Many-to-one

In a many-to-one relationship, each entity in one entity set is related to many entities in the other entity set. For example, a person can have many bank accounts and a bank account can belong to only one person.

- Entity in A associates with at most one entity in B, where A & B are entity sets and an entity of B is associated with at most one entity of A.
- Ratio of entities in A to entities in B is M:1.
- Eg - Student can enroll in many courses and a course can have many students enrolled in it or a student can enroll in many courses and a course can have many students enrolled in it.


<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/25.png?raw=true" alt="example"  >
                        <img  className="bg-purple-900 dark:bg-stone-900"  align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/25.png?raw=true" alt="example" />
                    </PhotoView>


###### ℹ️ Many-to-many

In a many-to-many relationship, each entity in one entity set is related to many entities in the other entity set. For example, a person can have many bank accounts and a bank account can belong to only one person.
- Entity in A associates with at most one entity in B, where A & B are entity sets and an entity of B is associated with at most one entity of A.
- Ratio of entities in A to entities in B is M:M.
- Eg - Student can enroll in many courses and a course can have many students enrolled in it or a student can enroll in many courses and a course can have many students enrolled in it.
- Another Ex: Employee is assigned to many projects and a project can have many employees assigned to it.



<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/26.png?raw=true" alt="example"  >
                        <img  className="bg-purple-900 dark:bg-stone-900"  align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/26.png?raw=true" alt="example" />
                    </PhotoView>
                </PhotoProvider>

</div>


#### ❓ Participation Constraints



Participate constraints are two types as mentioned below −

- Total participation

- Partial Participation

###### ℹ️ Total participation

In total participation, each entity in one entity set is related to many entities in the other entity set. For example, a person can have many bank accounts and a bank account can belong to only one person.

Example of total participation:
Every customer must have a loan account and every loan account must belong to a customer.



- Weak entity has total participation constraint
- Strong entity may not have total participation constraint
- It specifies that each entity in the entity set must compulsorily participate in at least one relationship instance in that relationship set.
- That is why, it is also called as mandatory participation.
- Total participation is represented using a double line between the entity set and relationship set.



<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/27.png?raw=true" alt="example"  >
                        <img  className="bg-purple-900 dark:bg-stone-900"  align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/27.png?raw=true" alt="example" />
                    </PhotoView>
                </PhotoProvider>


Double line between the entity set “Student” and relationship set “Enrolled in” signifies total participation. It specifies that each student must be enrolled in at least one course.

###### ℹ️ Partial participation

In partial participation, each entity in one entity set is related to many entities in the other entity set. For example, a person can have many bank accounts and a bank account can belong to only one person.



Example of partial participation:
A customer may have multiple loans but not all customers take out loans.

- It specifies that each entity in the entity set may or may not participate in the relationship instance in that relationship set.
- That is why, it is also called as optional participation.
- Partial participation is represented using a single line between the entity set and relationship set.



<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/27.png?raw=true" alt="example"  >
                        <img  className="bg-purple-900 dark:bg-stone-900"  align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/03.%20Data%20Model/img/27.png?raw=true" alt="example" />
                    </PhotoView>

Here,

Single line between the entity set “Course” and relationship set “Enrolled in” signifies partial participation.
It specifies that there might exist some courses for which no enrollments are made.


###### 🚩 Relationship

**Relationship between Cardinality and Participation Constraints**-


Minimum cardinality tells whether the participation is partial or total.

- If minimum cardinality = 0, then it signifies partial participation.
- If minimum cardinality = 1, then it signifies total participation.

Maximum cardinality tells the maximum number of entities that participates in a relationship set.



## ⭐ ER Notation



Symbols used in ER diagrams are as follows −

- Entity -> Rectangle
- Weak Entity -> Rectangle with double border
- Attribute -> Oval
- Multivalued Attribute -> Oval with double border
- Primary Key -> Oval with underline
- Weak Entity Key -> Oval with dotted underline
- Derived Attribute -> Oval with dotted border
- Relationship -> Diamond
- Relationship Set -> Diamond with double border
- Relationship Attribute -> Diamond with dotted border
- Total Participation -> Double line between entity and relationship
- Partial Participation -> Single line between entity and relationship
       

<PhotoView   src="https://images.edrawsoft.com/articles/er-diagram-symbols/chens-notation-1.png" alt="example"  >
                        <img  className="bg-purple-900 dark:bg-stone-900"  align="center"  src="https://images.edrawsoft.com/articles/er-diagram-symbols/chens-notation-1.png" alt="example" />
                    </PhotoView>
                </PhotoProvider>
 



