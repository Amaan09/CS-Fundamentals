## DBMS

**1.	What is DBMS ? How it is Different from Data Structures.**

Data Structure is about storing data or handling data into RAM or Temporary Memory. where Database is concept or tool which store & handle data at permanent memory location (Hard Drive)

Data structure is not permanent storage. It is alive till the program is alive. But we can use the different data structure to add data into database.

we use Database to store Data Structure containing process data at the end of any process .

Your shopping items are organized linearly into an array.

Your company's org chart is modeled in a tree.

Facebook connections are organized as a huge graph.


**2.	Difference Between Database and Database Management System ?**

 	 	 	
1. 	Storage: 	Besides computers, databases can even be maintained in physical ledgers, books or papers. 	In a database management system (DBMS), all the records are maintained only on a computer.

2. 	Data Retrieval: 	The retrieval of information from the databases can be done manually, through queries or by using programs (C, C++, Java etc.). 	We can retrieve the data from the database management system through queries written in SQL.

3. 	Speed: 	As databases can be handled manually or via computers, when SQL is not used to retrieve information, it can be very slow. 	As a computer system is involved in a database management system, the retrieval of information is very quick.

4. 	Access: 	The databases are not designed for a large number of people who can access data at the same time, rather it is designed for a very small number of people (preferably few people) who access data at different times. 	The database management system is designed for a large number of people who can access the data at the same time.

5. 	Data Manipulation: 	In case of the databases, very less information can be modified at a time. 	In the database management system (DBMS), a lot of information can be changed at one time (as it can have many users using it at the same time).

6. 	Backup and Recovery: The databases do not ensure that the data will be available after failure arises. 	The database management system (DBMS) ensures that the data will always be available even after system failures.

**3.	Main Memory and Secondary Memory.**

1. 	Primary memory is temporary. Secondary memory is permanent.

2. 	Primary memory is directly accessible by Processor/CPU. Secondary memory is not directly accessible by the CPU.
3. 	Nature of Parts of Primary memory varies, RAM- volatile in nature. ROM- Non-volatile. 	It’s always Non-volatile in nature.
4. 	Primary memory devices are more expensive than secondary storage devices. 	Secondary memory devices are less expensive when compared to primary memory devices.
5. 	The memory devices used for primary memory are semiconductor memories. 	The secondary memory devices are magnetic and optical memories.
6. 	Primary memory is also known as Main memory or Internal memory. 	Secondary memory is also known as External memory or Auxiliary memory.
7. 	Examples: RAM, ROM, Cache memory, PROM, EPROM, Registers, etc. 	Examples: Hard Disk, Floppy Disk, Magnetic Tapes, etc.

**4.	Basic Functionality and Advantages of DBMS i.e. Data Retrieve , Delete , Insert (Functionality) and Remove Redundancy , Easy access ( Advantages)**

**Reducing Data Redundancy**

The file based data management systems contained multiple files that were stored in many different locations in a system or even across multiple systems. Because of this, there were sometimes multiple copies of the same file which lead to data redundancy. 

This is prevented in a database as there is a single database and any change in it is reflected immediately. Because of this, there is no chance of encountering duplicate data.

**Sharing of Data**

In a database, the users of the database can share the data among themselves. There are various levels of authorisation to access the data, and consequently the data can only be shared based on the correct authorisation protocols being followed. 

Many remote users can also access the database simultaneously and share the data between themselves.

**Data Integrity**

Data integrity means that the data is accurate and consistent in the database. Data Integrity is very important as there are multiple databases in a DBMS. All of these databases contain data that is visible to multiple users. So it is necessary to ensure that the data is correct and consistent in all the databases and for all the users. 

**Data Security**

Data Security is vital concept in a database. Only authorised users should be allowed to access the database and their identity should be authenticated using a username and password. Unauthorised users should not be allowed to access the database under any circumstances as it violates the integrity constraints.

**Privacy**

The privacy rule in a database means only the authorized users can access a database according to its privacy constraints. There are levels of database access and a user can only view the data he is allowed to. For example - In social networking sites, access constraints are different for different accounts a user may want to access.

**Backup and Recovery**

Database Management System automatically takes care of backup and recovery. The users don't need to backup data periodically because this is taken care of by the DBMS. Moreover, it also restores the database after a crash or system failure to its previous condition. 

**Data Consistency**

Data consistency is ensured in a database because there is no data redundancy. All data appears consistently across the database and the data is same for all the users viewing the database. Moreover, any changes made to the database are immediately reflected to all the users and there is no data inconsistency.

**5.	DBMS Two Level and Three Level Architecture.**

**Two tier architecture:**

Two tier architecture is similar to a basic client-server model. The application at the client end directly communicates with the database at the server side. API’s like ODBC,JDBC are used for this interaction. The server side is responsible for providing query processing and transaction management functionalities. On the client side, the user interfaces and application programs are run. The application on the client side establishes a connection with the server side in order to communicate with the DBMS.
An advantage of this type is that maintenance and understanding is easier, compatible with existing systems. However this model gives poor performance when there are a large number of users.

**Three Tier architecture:**

In this type, there is another layer between the client and the server. The client does not directly communicate with the server. Instead, it interacts with an application server which further communicates with the database system and then the query processing and transaction management takes place. This intermediate layer acts as a medium for exchange of partially processed data between server and client. This type of architecture is used in case of large web applications.
Advantages:

    Enhanced scalability due to distributed deployment of application servers. Now,individual connections need not be made between client and server.
    Data Integrity is maintained. Since there is a middle layer between client and server, data corruption can be avoided/removed.
    Security is improved. This type of model prevents direct interaction of the client with the server thereby reducing access to unauthorized data.

**Disadvantages:**

Increased complexity of implementation and communication. It becomes difficult for this sort of interaction to take place due to presence of middle layers.

**6.	Entity Relationship Model (ER Model , Know the Basics i.e What is Entity , Attributes and Cardinality) (Hint : They won’t ask You to make Complex ER diagram)**

An entity can be a real-world object, either animate or inanimate, that can be easily identifiable. Entities are represented by means of their properties, called attributes. All attributes have values. For example, a student entity may have name, class, and age as attributes.

Types of Attributes

    Simple attribute − Simple attributes are atomic values, which cannot be divided further. For example, a student's phone number is an atomic value of 10 digits.

    Composite attribute − Composite attributes are made of more than one simple attribute. For example, a student's complete name may have first_name and last_name.

    Derived attribute − Derived attributes are the attributes that do not exist in the physical database, but their values are derived from other attributes present in the database. For example, average_salary in a department should not be saved directly in the database, instead it can be derived. For another example, age can be derived from data_of_birth.

    Single-value attribute − Single-value attributes contain single value. For example − Social_Security_Number.

    Multi-value attribute − Multi-value attributes may contain more than one values. For example, a person can have more than one phone number, email_address, etc.

Cardinality defines the number of entities in one entity set, which can be associated with the number of entities of other set via relationship set.

    One-to-one − One entity from entity set A can be associated with at most one entity of entity set B and vice versa.
    One-to-one relation

    One-to-many − One entity from entity set A can be associated with more than one entities of entity set B however an entity from entity set B, can be associated with at most one entity.
    One-to-many relation

    Many-to-one − More than one entities from entity set A can be associated with at most one entity of entity set B, however an entity from entity set B can be associated with more than one entity from entity set A.
    Many-to-one relation

    Many-to-many − One entity from A can be associated with more than one entity from B and vice versa.

![Image of ER](https://www.tutorialspoint.com/dbms/images/er_attributes_derived.png)

* Entities are represented by means of rectangles.
* Attributes are represented by means of ellipses.
* Composite attributes are represented by ellipses that are connected with an ellipse.
* Multivalued attributes are depicted by double ellipse.
* Derived attributes are depicted by dashed ellipse.

**7.	Relational Model ( Difference b/w ER model and Relational Model)**

1. 	ER model is the high level or conceptual model. It is the representational or implementation model.

2. 	It is used by people who don’t know how database is implemented. It is used by programmers.

3. 	It represents collection of entities and describes relationship between them. It represent data in the form of tables and describes relationship between them.

4. 	It consists of components like Entity, Entity Type, Entity Set. It consists of components like domain, attributes, tuples.

5. 	It is easy to understand the relationship between entities. It is less easy to derive the relationship between different tables.

6. 	It describes cardinality. It does not describes cardinality.

**8.	All type of Keys in Relational Model ( Primary Key , Super Key , Candidate Key , Foreign Key) (Hint : Important)**

**Candidate Key:** 

The minimal set of attribute which can uniquely identify a tuple is known as candidate key. For Example, STUD_NO in STUDENT relation.

    The value of Candidate Key is unique and non-null for every tuple.
    There can be more than one candidate key in a relation. For Example, STUD_NO is candidate key for relation STUDENT.
    The candidate key can be simple (having only one attribute) or composite as well. For Example, {STUD_NO, COURSE_NO} is a composite candidate key for relation STUDENT_COURSE.

**Super Key:** 

The set of attributes which can uniquely identify a tuple is known as Super Key. For Example, STUD_NO, (STUD_NO, STUD_NAME) etc.

    Adding zero or more attributes to candidate key generates super key.
    A candidate key is a super key but vice versa is not true.

**Primary Key:** 

There can be more than one candidate key in relation out of which one can be chosen as the primary key. For Example, STUD_NO, as well as STUD_PHONE both, are candidate keys for relation STUDENT but STUD_NO can be chosen as the primary key (only one out of many candidate keys).

**Alternate Key:** 

The candidate key other than the primary key is called an alternate key. For Example, STUD_NO, as well as STUD_PHONE both, are candidate keys for relation STUDENT but STUD_PHONE will be alternate key (only one out of many candidate keys).

**Foreign Key:** 

If an attribute can only take the values which are present as values of some other attribute, it will be a foreign key to the attribute to which it refers. The relation which is being referenced is called referenced relation and the corresponding attribute is called referenced attribute and the relation which refers to the referenced relation is called referencing relation and the corresponding attribute is called referencing attribute. The referenced attribute of the referenced relation should be the primary key for it. For Example, STUD_NO in STUDENT_COURSE is a foreign key to STUD_NO in STUDENT relation.

It may be worth noting that unlike, Primary Key of any given relation, Foreign Key can be NULL as well as may contain duplicate tuples i.e. it need not follow uniqueness constraint.

For Example, STUD_NO in STUDENT_COURSE relation is not unique. It has been repeated for the first and third tuple. However, the STUD_NO in STUDENT relation is a primary key and it needs to be always unique and it cannot be null.

**9.	Armstrong Axioms and All type of Functional Dependencies (Transitive and Relative)**


    Axiom of Reflexivity:
    If a set of attributes is P and its subset is Q, then P holds Q. If Q ⊆ P, then P → Q. This property is called as Trivial functional dependency. Where P holds Q (P → Q) denote P functionally decides Q.
    Axiom of Augmentation:
    If P holds Q (P → Q) and R is a set of attributes, then PR holds QR (PR → QR). It means that a change in attributes in dependencies does not create a change in basic dependencies. If P → Q, then PR → QR for any R.
    Axiom of Transitivity:
    If P holds Q (P → Q) and Q holds R (Q → R), then P hold R (P → R). Where P holds R (P → R) denote P functionally decides R, same with P holds Q and Q holds R.

2) Additional rules or secondary rules

These rules can be derived from the above axioms.

    Union:
    If P holds Q (P → Q) and P holds R (P → R), then P → QR. If X → Y and X → Z, then X → YZ.
    Composition:
    If P holds Q (P → Q) and A holds B (A → B), then PA → QB.
    Decomposition:
    This rule is contrary of union rule. If P → QR, then P holds Q (P → Q) and P holds R (P → R). If X → YZ, then X → Y and X → Z.
    Pseudo Transitivity:
    If P → RQ and Q → S, then P → RS.

Trivial Functional Dependency

Trivial 	

If P holds Q (P → Q), where P is a subset of Q, then it is called a Trivial Functional Dependency. Trivial always holds Functional Dependency.

Non-Trivial 	

If P holds Q (P → Q), where Q is not a subset of P, then it is called as a Non-Trivial Functional Dependency.

Completely Non-Trivial 	

If P holds Q (P → Q), where P intersect Y = Φ, it is called as a Completely Non-Trivial Functional Dependency.

**10.	Database Anomalies ( Insert , Delete and Update)**

**Insertion anomaly:** 

If a tuple is inserted in referencing relation and referencing attribute value is not present in referenced attribute, it will not allow inserting in referencing relation. For Example, If we try to insert a record in STUDENT_COURSE with STUD_NO =7, it will not allow.

**Deletion and Updation anomaly:** 

If a tuple is deleted or updated from referenced relation and referenced attribute value is used by referencing attribute in referencing relation, it will not allow deleting the tuple from referenced relation. For Example, If we try to delete a record from STUDENT with STUD_NO =1, it will not allow. To avoid this, following can be used in query:


    ON DELETE/UPDATE SET NULL: If a tuple is deleted or updated from referenced relation and referenced attribute value is used by referencing attribute in referencing relation, it will delete/update the tuple from referenced relation and set the value of referencing attribute to NULL.
    ON DELETE/UPDATE CASCADE: If a tuple is deleted or updated from referenced relation and referenced attribute value is used by referencing attribute in referencing relation, it will delete/update the tuple from referenced relation and referencing relation as well.

**11.	Normalization -> What is Normalization ? Why do we need Normalization ?**

* If a database design is not perfect, it may contain anomalies, which are like a bad dream for any database administrator. Managing a database with anomalies is next to impossible.
* Normalization is a method to remove all these anomalies and bring the database to a consistent state.


**12.	All the Types of Normalization , 1NF , 2NF , 3NF and BCNF. (Hint : They won’t ask you to Convert the Functions into 1NF , 2NF and All , Just Know the Basics of Each Normal Form & It Would Be Better if you Understand Every NF Form with an Example) (Important topic)**

**First Normal Form**

First Normal Form is defined in the definition of relations (tables) itself. This rule defines that all the attributes in a relation must have atomic domains. The values in an atomic domain are indivisible units.

**Second Normal Form**

Before we learn about the second normal form, we need to understand the following −

    Prime attribute − An attribute, which is a part of the candidate-key, is known as a prime attribute.

    Non-prime attribute − An attribute, which is not a part of the prime-key, is said to be a non-prime attribute.

If we follow second normal form, then every non-prime attribute should be fully functionally dependent on prime key attribute. That is, if X → A holds, then there should not be any proper subset Y of X, for which Y → A also holds true.

Not in 2NF

```
Table - 1
Student Id| Project Id | Student Name | Project Name
```
In 2NF

```
Table - 1
Student Id| Student Name

Table - 2
Student Id| Project Id | Project Name

```
**Third Normal Form**

For a relation to be in Third Normal Form, it must be in Second Normal form and the following must satisfy −

    No non-prime attribute is transitively dependent on prime key attribute.
    For any non-trivial functional dependency, X → A, then either −
        X is a superkey or,
        A is prime attribute.

```
Table - 1
Student Id| Student Name | City | Zip
```
```
Table - 1
Student Id| Student Name | Zip

Table - 2
Zip| City

```


**Boyce-Codd Normal Form**

Boyce-Codd Normal Form (BCNF) is an extension of Third Normal Form on strict terms. BCNF states that −

    For any non-trivial functional dependency, X → A, X must be a super-key.



**13.	SQL Queries ( Learn with one example of Each Query , Not Much, Best Resource : SQL w3 Resource )**

[SQL queries link](https://www.codecademy.com/learn/learn-sql/modules/learn-sql-multiple-tables/cheatsheet)

**14.	File Structures in Database ( Indexing , Sparse Indexing , B- Tree , B+ trees) (Source GFG)**

**Sequential File Organization –**

The easiest method for file Organization is Sequential method. In this method the file are stored one after another in a sequential manner.

Pros –

    Fast and efficient method for huge amount of data.
    Simple design.
    Files can be easily stored in magnetic tapes i.e cheaper storage mechanism.

Cons –

    Time wastage as we cannot jump on a particular record that is required, but we have to move in a sequential manner which takes our time.
    Sorted file method is inefficient as it takes time and space for sorting records.

**Heap File Organization –**

Heap File Organization works with data blocks. In this method records are inserted at the end of the file, into the data blocks. No Sorting or Ordering is required in this method. If a data block is full, the new record is stored in some other block, Here the other data block need not be the very next data block, but it can be any block in the memory. It is the responsibility of DBMS to store and manage the new records.

Pros –

    Fetching and retrieving records is faster than sequential record but only in case of small databases.
    When there is a huge number of data needs to be loaded into the database at a time, then this method of file Organization is best suited.

Cons –

    Problem of unused memory blocks.
    Inefficient for larger databases.

**Hash File Organization :**

Hashing is an efficient technique to directly search the location of desired data on the disk without using index structure. Data is stored at the data blocks whose address is generated by using hash function. The memory location where these records are stored is called as data block or data bucket. 


    Data bucket – Data buckets are the memory locations where the records are stored. These buckets are also considered as Unit Of Storage.
    Hash Function – Hash function is a mapping function that maps all the set of search keys to actual record address. Generally, hash function uses primary key to generate the hash index – address of the data block. Hash function can be simple mathematical function to any complex mathematical function.
    Hash Index-The prefix of an entire hash value is taken as a hash index. Every hash index has a depth value to signify how many bits are used for computing a hash function. These bits can address 2n buckets. When all these bits are consumed ? then the depth value is increased linearly and twice the buckets are allocated.

**B+ Tree File Organization –**

B+ Tree, as the name suggests, It uses a tree like structure to store records in File. It uses the concept of Key indexing where the primary key is used to sort the records. For each primary key, an index value is generated and mapped with the record. An index of a record is the address of record in the file.

B+ Tree is very much similar to binary search tree, with the only difference that instead of just two children, it can have more than two. All the information is stored in leaf node and the intermediate nodes acts as pointer to the leaf nodes. The information in leaf nodes always remain a sorted sequential linked list.

Pros –

    Tree traversal is easier and faster.
    Searching becomes easy as all records are stored only in leaf nodes and are sorted sequential linked list.
    There is no restriction on B+ tree size. It may grows/shrink as the size of data increases/decreases.

Cons –

    Inefficient for static tables.

**Cluster File Organization –**

In cluster file organization, two or more related tables/records are stored withing same file known as clusters. These files will have two or more tables in the same data block and the key attributes which are used to map these table together are stored only once.

Thus it lowers the cost of searching and retrieving various records in different files as they are now combined and kept in a single cluster.
For example we have two tables or relation Employee and Department. These table are related to each other.

Therefore these table are allowed to combine using a join operation and can be seen in a cluster file.

If we have to insert, update or delete any record we can directly do so. Data is sorted based on the primary key or the key with which searching is done. Cluster key is the key with which joining of the table is performed.

**15.	Transactions , Operations of Transactions , Transaction’s ACID Properties (Important)**

A transaction can be defined as a group of tasks. A single task is the minimum processing unit which cannot be divided further.

Let's take an example of a simple transaction. Suppose a bank employee transfers Rs 500 from A's account to B's account. This very simple and small transaction involves several low-level tasks.

A’s Account

```
Open_Account(A)
Old_Balance = A.balance
New_Balance = Old_Balance - 500
A.balance = New_Balance
Close_Account(A)
```

B’s Account

```
Open_Account(B)
Old_Balance = B.balance
New_Balance = Old_Balance + 500
B.balance = New_Balance
Close_Account(B)
```
**ACID Properties**

    Atomicity − This property states that a transaction must be treated as an atomic unit, that is, either all of its operations are executed or none. There must be no state in a database where a transaction is left partially completed. States should be defined either before the execution of the transaction or after the execution/abortion/failure of the transaction.

    Consistency − The database must remain in a consistent state after any transaction. No transaction should have any adverse effect on the data residing in the database. If the database was in a consistent state before the execution of a transaction, it must remain consistent after the execution of the transaction as well.

    Durability − The database should be durable enough to hold all its latest updates even if the system fails or restarts. If a transaction updates a chunk of data in a database and commits, then the database will hold the modified data. If a transaction commits but the system fails before the data could be written on to the disk, then that data will be updated once the system springs back into action.

    Isolation − In a database system where more than one transaction are being executed simultaneously and in parallel, the property of isolation states that all the transactions will be carried out and executed as if it is the only transaction in the system. No transaction will affect the existence of any other transaction.

**16.	State of Transactions i.e Committed , partially Committed**

![Image of Transactions](https://www.tutorialspoint.com/dbms/images/transaction_states.png)

    Active − In this state, the transaction is being executed. This is the initial state of every transaction.

    Partially Committed − When a transaction executes its final operation, it is said to be in a partially committed state.

    Failed − A transaction is said to be in a failed state if any of the checks made by the database recovery system fails. A failed transaction can no longer proceed further.

    Aborted − If any of the checks fails and the transaction has reached a failed state, then the recovery manager rolls back all its write operations on the database to bring the database back to its original state where it was prior to the execution of the transaction. Transactions in this state are called aborted. The database recovery module can select one of the two operations after a transaction aborts −
        Re-start the transaction
        Kill the transaction

    Committed − If a transaction executes all its operations successfully, it is said to be committed. All its effects are now permanently established on the database system.



**17.	Concurrency Control , Lock and all over Transactions**

* Concurrency control is the procedure in DBMS for managing simultaneous operations without conflicting with each another. 

Example

```
Assume that two people who go to electronic kiosks at the same time to buy a movie ticket for the same movie and the same show time.

However, there is only one seat left in for the movie show in that particular theatre. Without concurrency control, it is possible that both moviegoers will end up purchasing a ticket. However, concurrency control method does not allow this to happen. Both moviegoers can still access information written in the movie seating database. But concurrency control only provides a ticket to the buyer who has completed the transaction process first. 
```

**Concurrency Control Protocols**

Lock-based Protocols

A lock is a data variable which is associated with a data item..

All lock requests are made to the concurrency-control manager. Transactions proceed only once the lock request is granted.

1. Shared Lock (S):

A shared lock is also called a Read-only lock.

2. Exclusive Lock (X):

With the Exclusive Lock, a data item can be read as well as written. 

* Starvation is the situation when a transaction needs to wait for an indefinite period to acquire a lock. 
* Deadlock refers to a specific situation where two or more processes are waiting for each other to release a resource or more than two processes are waiting for the resource in a circular chain. 

Two Phase Locking (2PL) Protocol

Two-Phase locking protocol which is also known as a 2PL protocol. It is also called P2L. In this type of locking protocol, the transaction should acquire a lock after it releases one of its locks.

This locking protocol divides the execution phase of a transaction into three different parts.

    In the first phase, when the transaction begins to execute, it requires permission for the locks it needs.
    The second part is where the transaction obtains all the locks. When a transaction releases its first lock, the third phase starts.
    In this third phase, the transaction cannot demand any new locks. Instead, it only releases the acquired locks.

**Timestamp-based Protocols**

* The timestamp-based algorithm uses a timestamp to serialize the execution of concurrent transactions.
* The older transaction is always given priority in this method. 
