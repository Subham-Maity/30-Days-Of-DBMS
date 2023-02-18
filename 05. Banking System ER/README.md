# [Website View](https://code-xam.vercel.app/docs/dbms/dbms5)


## ⭐ Make ER Diagram


Steps to make ER Diagram



1. Identify entities
   - Determine the real-world objects or concepts that will be part of the system
   - Entities should be able to be identified uniquely

2. Define attributes
   - For each entity, define the properties or characteristics that describe it
   - Attributes should be specific and relevant to the entity

3. Determine relationships
   - Identify how the entities are connected and interact with each other
   - Determine the type of relationship, such as one-to-one, one-to-many, or many-to-many

4. Draw the ER diagram
   - Use boxes or rectangles to represent entities and their attributes
   - Use lines or diamonds to represent the relationships between entities

5. Add points
   - Include additional information about the entities or relationships as notes or points on the diagram
   - Provide any constraints or rules that apply to the entities or relationships

6. Validate and refine the ER diagram
   - Review the diagram to ensure it accurately represents the system being modeled
   - Make any necessary changes or adjustments to improve the diagram's accuracy and usability.


## ⭐ Requirement Engineering

<div className= "mt-3"></div>
<div className="cardTexture5">
    <h1 style={{padding: "8px"}} className = "mb-8 text-center font-bold text-transparent sm:text-4xl text-[25px] tex bg-clip-text bg-[radial-gradient(ellipse_at_top_left,_var(--tw-gradient-stops))] from-sky-700 via-cyan-500 to-neutral-300" align="middle">
        Requirements of Banking System

</h1>




1. Banking system → Branches


> Bank may have multiple branches


2. Bank → customers.


> Bank has multiple customers




3. Customers → accounts & take loans.



> Customer may have multiple accounts & take multiple loans


4. Customer associated with some banker.



> Customer may be associated with multiple bankers means when you deal with loan you need manager or branch manager or some banker.



5. Bank has employees.

> Bank has multiple employees


6. Account → Savings, Current, FD, RD, Loan Account

> Account may be of multiple types like savings, current, FD, RD, Loan Account

7. Loan originated by branch.
    loan = multiple customers
    → Payment schedulePayment schedule


>  Loan may be originated by multiple branches and multiple customers also have multiple payment schedules.

>  Payment schedule may be of multiple types like monthly, quarterly, half yearly, yearly.





## ⭐ Steps to Visualize

<div className= "mt-3"></div>
<div className="cardTexture5">
    <h1 style={{padding: "8px"}} className = "mb-8 text-center font-bold text-transparent sm:text-4xl text-[25px] tex bg-clip-text bg-[radial-gradient(ellipse_at_top_left,_var(--tw-gradient-stops))] from-sky-700 via-cyan-500 to-neutral-300" align="middle">
        How to identify Entity & Attribute sets

</h1>


We think this DB as bottom up approach. So we will start from weakest entity set and then we will move to strong entity set.

### Step 1

<p className="text-amber-900 dark:text-amber-200 font-bold mb-4 mt-8"> Entity Sets </p>

**1.** Branch

**2.** Customer

**3.** Employee

**4.** Savings A/C (Account Entity Set) → Generalization

**5.** Current A/C (Account Entity Set) → Generalization

**6.** Loan

**7.** Payment (loan) → Weakest entity set


### Step 2
<p className="text-amber-900 dark:text-amber-200 font-bold mb-4 mt-8"> Attributes </p>



<u > 1.**Branch** </u> → Branch ID, <Mark type="error">Branch Name (primary key)</Mark>, Branch Address, Branch Manager , Liability, Assets, City, State, Country


<u >2. Customer </u> → <Mark type="error">Cust-id (primary key)</Mark>, Name , <Mark type="error">Address(Composite Attribute) </Mark>, <Mark type="info">Contact no(Multi Valued)</Mark> , DOB , <Mark type="info">Age(Derived Attribute)</Mark>

<u>3. Employee </u> →<Mark type="error"> Emp-id (primary key)</Mark>, Name , <Mark type="info">Contact no(Single Valued)</Mark> , <Mark type="info">Department Name(Multi Valued)</Mark> , <Mark type="info">Years of Service (Derived Valued) </Mark>,  <Mark type="info">Start Date(Single Valued)</Mark>

<u>4. Savings A/C </u> → <Mark type="error"> Acc-Number(primary key)</Mark> , balance , interest rate , daily interest limit

<u>5. Current A/C </u> →  <Mark type="error">Acc-Number (primary key)</Mark>, balance , Per transaction charge , overdraft amount

<u>6. Generalized Entity "Account" </u> → Acc-No , Balance

> We have generalized Account entity set because both Savings A/C and Current A/C have same attributes.

<u>7. Loan </u> →  <Mark type="error"> loan-number(primary key)</Mark> , amount

<u>8. Weak Entity "Payment" </u> → payment-number , amount , date

### Step 3

<p className="text-amber-900 dark:text-amber-200 font-bold mb-4 mt-8"> Relationships & Constraints </p>

#### 1. Customer & Loan

<u>Mapping Cardinality </u>

- Customer ``<borrow>`` Loan → many to many (M : N)

> Customer can borrow multiple loans and loan can be borrowed by multiple customers.

<u> Participation Constraints </u>

- `loan` and `borrow` is total participation constraint because if loan is exist then customer must be exist and vice versa.


#### 2. Loan & Branch

<u>Mapping Cardinality </u>

- Loan ``<originated by>`` Branch → many to one (n : 1)

> Loan can be originated by only one branch and one branch can originate multiple loans.

<u> Participation Constraints </u>

- `loan` and `originated by` is total participation constraint because if loan is exist then branch must be exist and vice versa.

#### 3. Loan & Payment (weak relationship)

If we have a weak entity set in a database, and it participates in a relationship with another weak entity set, then this relationship is considered a weak relationship. To properly model this relationship, we should apply a total participation constraint to the weak entity set that participates in the relationship.



<u>Mapping Cardinality </u>

- Loan ``<has>`` Payment → one to many (1 : n)

> Loan can have multiple payments and payment can be associated with only one loan.

<u> Participation Constraints </u>

- `loan` and `has` is total participation constraint because if loan is exist then payment must be exist and vice versa.

#### 4. Customer & Account

<u>Mapping Cardinality </u>

- Customer ``<depsit>`` Account → many to many (M : N)

> Customer can deposit multiple accounts and account can be deposited by multiple customers.

<u> Participation Constraints </u>

- `account` and `deposit` is total participation constraint because if account is exist then customer must be exist and vice versa.

#### 5. Customer & Banker

<u>Mapping Cardinality </u>

- Customer ``<associated with>`` Banker → many to one (N : 1)

> Customer can be associated with multiple bankers and banker can be associated with multiple customers.

<u> Participation Constraints </u>

- `customer` and `associated with` is total participation constraint because if customer is exist then banker must be exist and vice versa.

#### 6. Employee & Employee (Unary Relationship)

<u>Mapping Cardinality </u>

- Employee ``<managed by>`` Employee → many to one (N : 1)

> Employee can be managed by multiple employees and employee can be managed by multiple employees.

<u> Participation Constraints </u>

- `employee` and `managed by` is total participation constraint because if employee is exist then employee must be exist and vice versa.


</h11>
</div>


## ⭐ Create ER Diagram

### Bank Management System ER Diagram


<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/05.%20Banking%20System%20ER/Files/Banking%20SYSTEM.png?raw=true" alt="example" >
                    <img  className="bg-purple-300 dark:bg-stone-800" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/05.%20Banking%20System%20ER/Files/Banking%20SYSTEM.png?raw=true" alt="example" />
                </PhotoView>
            </PhotoProvider>
  



## ⭐ Another ER Diagram



### Online Ordering System ER Diagram

<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/05.%20Banking%20System%20ER/Files/Online%20Ordering%20System.png?raw=true" alt="example" >
                    <img  className="bg-purple-300 dark:bg-stone-300" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/05.%20Banking%20System%20ER/Files/Online%20Ordering%20System.png?raw=true" alt="example" />
                </PhotoView>
            </PhotoProvider>
            <figcaption>
                Change the image size by using the click-and-scroll function.
            </figcaption>
        </figure>
        </div>


### Voting System ER Diagram


<PhotoView   src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/05.%20Banking%20System%20ER/Files/voting%20system%20ERD.png?raw=true" alt="example" >
                    <img  className="bg-purple-300 dark:bg-stone-300" style={{ position: "relative" ,opacity: 1 ,borderRadius: "10px" ,overflow: "hidden" , marginTop:"20px" , marginBottom: "20px"}} align="center"  src="https://github.com/Subham-Maity/30-Days-Of-DBMS/blob/main/05.%20Banking%20System%20ER/Files/voting%20system%20ERD.png?raw=true" alt="example" />
                </PhotoView>
            </PhotoProvider>



