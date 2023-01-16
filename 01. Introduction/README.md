# [Website View](https://code-xam.vercel.app/docs/dbms/dbms1)

⭐ What is Data ?[](#-what-is-data-)
-----------------------------------

![](https://media.giphy.com/media/N1TzDcgCw0m2Lors1I/giphy.gif)

let's say you own a small bakery and you want to keep track of your sales and customer information. Each day, you write down the number of cupcakes, cookies, and cakes sold, as well as the names and contact information of customers who make a purchase.

This information is raw data because it doesn't tell you anything meaningful on its own. But, once you organize it and make sense of it, it can give you valuable insights into your business. For example, you might notice that you sell more cupcakes on weekends than on weekdays, or that a certain customer always buys cookies whenever they visit.

![](https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/01.%20Introduction/img/change1.png?raw=true)

So in this example, the raw data that you collect on your bakery sales and customer information is similar to the pile of puzzle pieces. It doesn't make sense on its own, but once you organize it and make sense of it, you can use it to make better decisions and improve your business.

Then what is data? 😥❓

a. Data is a collection of raw, unorganized facts and details like text, observations, figures, symbols, and descriptions of things etc. In other words, data does not carry any specific purpose and has no significance by itself. Moreover, data is measured in terms of bits and bytes – which are basic units of information in the context of computer storage and processing.

b. Data can be recorded and does’t have any meaning unless processed.

⭐ Types of Data ?[](#-types-of-data-)
-------------------------------------

![](https://media.giphy.com/media/HGzsY5vgQ0iNiCWn4f/giphy.gif)

Types of Data ? 😥❓

**a. Quantitative**

i. Numerical form

ii. Weight, volume, cost of an item.

**b. Qualitative**

i. Descriptive, but not numerical.

ii. Name, gender, hair color of a person.

Quantitative data is data that can be measured and expressed in numbers. For example, the weight of an object, the volume of a liquid, or the cost of an item are all examples of quantitative data. This data is numerical and can be used to make calculations and draw conclusions.

Qualitative data, on the other hand, is data that describes something but cannot be expressed in numbers. For example, the name, gender, or hair color of a person are all examples of qualitative data. This type of data is usually more descriptive and doesn't lend itself well to calculations or numerical analysis. It is more useful for understanding the context, meaning, and other non-numerical aspects of something.

⭐ What is Information ?[](#-what-is-information-)
-------------------------------------------------

![](https://media.giphy.com/media/UMyvk17PIo3SiZQWju/giphy.gif)

Imagine you are trying to plan a community event and you want to know more about the people living in your area. You might collect data about the number of people in different age groups, their genders, and how many babies have been born recently. This data is like a pile of puzzle pieces. It doesn't tell you anything useful until you organize it and make sense of it.

When you analyze and interpret this data, you might come to some conclusions, like "there are 100 senior citizens living in the area," "the gender ratio is 1.1," or "there are 100 newborn babies." These are examples of information. This information gives context to the data, and allows you to make decisions like how to design the event to be accessible and inclusive to seniors, and how to ensure the safety of newborns.

So, in short, information is the processed data that makes sense to us. It is extracted from data by analyzing and interpreting it. It is more meaningful than raw data and it enables decision making.

Then what is Information ? 😥❓

**a. Info. Is processed, organized, and structured data.**

**b. It provides context of the data and enables decision making.**

**c. Processed data that make sense to us.**

**d. Information is extracted from the data, by analyzing and interpreting pieces of data.**

**e. E.g.,you have data of all the people living in your locality, its Data, when you analyze and interpret the data and come to some conclusion that:**

*   i There are 100 senior citizens.
*   ii. The sex ratio is 1.1.
*   iii. Newborn babies are 100.

These are information.

⭐ Data vs Information[](#-data-vs-information)
----------------------------------------------

![](https://media.giphy.com/media/jFzojLrYSgJlGUuwq9/giphy.gif)

⭐ What is Database ?[](#-what-is-database-)
-------------------------------------------

![](https://media.giphy.com/media/TncmRRvEGVoVcHgaAb/giphy.gif)

let's say you're a teacher and you want to keep track of your students' grades. Instead of storing each student's grades in a separate file, you could use a database to organize all that information in one place. You could create a table with each student's name as a column and each assignment or test as a row. This way, you can easily search for a specific student's grades, or find the average grade for a certain assignment across the class.

So, in short, a database is an electronic place where data is stored in an organized way and it can be easily accessed, managed and updated.

Then what is Database ? 😥❓

a. Database is an electronic place/system where data is stored in a way that it can be easily accessed, managed, and updated.

b. To make real use Data, we need Database management systems.(DBMS)

⭐ What is DBMS ?[](#-what-is-dbms-)
-----------------------------------

![](https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/01.%20Introduction/img/2.png?raw=true)

Imagine you're the owner of a small retail store and you want to keep track of your inventory. You might use a database to store information about your products such as name, price, quantity, and location in the store. To manage and interact with this information, you would use a DBMS, which would provide you with tools and functionality to perform operations such as adding new products, checking current stock levels, updating prices, and removing items that are no longer in stock.

Then what is Database management systems.(DBMS) ? 😥❓

In short, a DBMS is a collection of programs and tools that are used to create, manage, and interact with a database. It allows you to perform various operations on the data stored in the database, like adding, accessing, updating and deleting the data, while ensuring that the data is accurate, consistent and secure.

⭐ What is DBMS vs File Systems ?[](#-what-is-dbms-vs-file-systems-)
-------------------------------------------------------------------

![](https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/01.%20Introduction/img/3.png?raw=true)

Imagine you are a small business owner and you keep track of all your customers' information in a big file cabinet. Each file in the cabinet represents a customer and contains their personal information, purchase history, and contact information. As your business grows, the cabinet becomes more cluttered and disorganized. It becomes difficult to find specific customer information, and you might even end up with multiple files for the same customer, leading to data redundancy and inconsistency. And if you want to make any changes to the customer information, it becomes difficult as you have to go through all the files to find the correct one.

On the other hand, if you use a DBMS, it would be like having a personal assistant to manage all your customer information. The DBMS would help you to organize the information in an efficient way, making it easy to access, update, and maintain. It would also prevent data redundancy and inconsistency, and ensure data integrity and security.

So in short, a DBMS is an electronic system that helps to manage and organize data efficiently, while a file system is a way to store and access data in a basic way, and it has major disadvantages like data redundancy, difficulty in accessing data and security problems.