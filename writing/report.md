### cs312s2022

Please add your responses to this file.

#### Lab 4 Assignment
#### Schema Design

#### Name
Favour Ojo


#### GitHub Account Name
favourojo

#### Submission Date
18 April 2022


Please answer the following questions using **clear and meaningful language**. It is expected that there will be at least 50 words per answer. Do not use one-liners to respond.


#### 1)

 - Describe the general functionality of your database. What is the database _supposed_ to do?

 ```
 This database shows classification on salary whether less than 50K or greater than 50K.

 ```

#### 2)

  - Explain your data: give the reference (or hyperlink) and discuss the purpose of the dataset. For instance, what is this data set? How was it collected? What information does it contain? What kind of trust can be placed in this dataset?

	```
	[Reference](https://www.kaggle.com/datasets/ayessa/salary-prediction-classification)

  This dataset is a prediction task to determine whether a person makes over 50k a year. Some of the factors spoke about is age, workclass, education, marital-status, occupation, etc,. The extraction of this data set was done by Barry Becker from the 1994 Census database.

	```

#### 3)
- Describe your database at the _View Schema_ level. How will users interact with the database? If the database were scaled-up to handle a larger set of data or more users, how would the _View Schema_ change if at all? Explain your thinking.

 ```
In the View Schema level, users will be able to see how the factors of each individual affects whether they make over or under 50K. With this, users will be able to make their own hypothesis about the database..

 ```

#### 4)
- Describe your database at the _Logical Schema_ level. Discuss the tables, attributes and the relationships that exist them and the other parts of the database.

 ```
 The tables each represent a significant part of the data set. The table Person describes the important characteristics of the individuals that were surveyed. With this table, an argument can be made that these certain characteristics that each individual has affects the salary that they are making. A connection can be made between all three tables because each table has an attribute that could potentially have an influence on the affect of salary. The table Work shows the type of jobs each individual in the Person table has and how much time is committed to said job. Lastly, the Education tables shows the type of education each individual has and how long they were in school.

 ```


#### 5)
 - Describe your database at the _Internal Schema_ level. What hardware is necessary to run this database? How would the schema change for a larger application of this database?
	```
	To run this this database, I believe a lot of memory is necessary. The actual data, without splitting it into 3 tables and condensing it, is very large and something that allows for a good amount of storage is needed for this type of data set. I believe any kind of machine would be sufficient to run this database. Only thing that would be needed to be downloaded would be SQLite and that is an easy download for all machines.

	```

#### 6)

 - Archival: Discuss how the data will be physically stored? What are the imitations of this storage system?

 ```
 I believe the best way to store this data would be by a hard drive. A hard drive is a very dependable piece of data storage and it can hold a huge amount of data that is needed.

 ```

#### 7a)

 - Ask an intelligent question _involving three of the tables_ and then give a query and result to answer that query.

  - Question

 	```
 	How many white people earn more less than or exactly 50K
 	```

  - Query

 	```
  SELECT COUNT(Person.race) FROM Person WHERE race == " White" AND salary == " <=50K";

 	```

  - Result

 	```
 	4

 	```


#### 7b)

- Ask another intelligent question _involving three of the tables_ and then give a query and result to answer that query.

 - Question

	```
	How many individuals work 40 hours work weeks?

	```

 - Query

	```
	SELECT COUNT(Work.hoursPerWeek) FROM Work WHERE hoursPerWeek == 40;

	```

 - Result

	```
	6

	```


---

Ethical

#### 8)

Imagine that your database schema was adopted by a hospital to be used as a system to manage all their past, current and future medical records.

Explain how easily it would be to add medical data to your current schema to create a functioning database. How could this medical data be fitted into your established schema? What problems would exist?

```
I believe it would be virtually pretty easy to add medical data to my current schema. I already have created a table that shows the characteristics of an individual, which I believe can be very helpful for a hospital because in a hospital, they always record your medical records. For instance, they always record your height, weight, race, sex, etc,. Some of those factors I already have in my own table.

```

#### 9)

 - Imagine that your database was successfully readapted to manage the hospital's medical records data (and is currently being used thanks to a few modifications). What is one of the largest concerns of privacy or security that you could imagine if the exact _logical schema_ was known by malicious users. Explain your thinking.

 ```
 Inside the data I was able to extract, there are certain attributes that could release someone's personal information. That would be my biggest concern with this database. It could be very dangerous if malicious users have possession of this kind of individuals' information.

 ```

#### 10)
 - Concerning the _view schema_ or _physical schema_ levels of the database, What security concerns for the data would become apparent if either of these levels were to become public knowledge?

```
The biggest security for the view schema level would be the basis of the information would be instantly viewable. In the view schema, all the different attributes are revealed. A malicious user could easily see if they are interested in seeing this information that is available from this data set. In the physical schema, the way to download this data set and the hardware that is needed to run this database.

```

#### 11)

- What kinds of data in this medical database would be best **not** to hold to prevent trouble in the event of a breach? Explain your thinking.

```
I believe the information contained in table Person would not be smart to hold to prevent trouble. Without this information, it makes the combined data set very confusing and no hypothesis can really be made when that information is missing.

```

#### 12)

 - Describe the most ideal way for a typical user to interact with this database. For instance, what kinds of skills and hardware would be necessary for the hospital staff to use the system?

 ```
 The type of skills an individual would need to possess to be able to interact with this database is first, a simple understanding of what SQLite is. Without understanding SQLite, it would be difficult to conduct analysis on the program and create queries. A suitable machine that will be able to download SQLite will be what is a necessary when it comes to hardware.

 ```


#### 13)

  - You have been told that all medical information is available to all users of the database, regardless of a user's role in the hospital. Is this a "feature" or a "flaw" in the design of the system? With this knowledge of general database use, what changes would you make to the system (if any) to fix this issue? Explain your thinking.

  ```
  I believe this is a flaw in the design of the system. It would be unethical for everyone in the hospital to have access to all the users of the database without the user's knowledge. I feel the best way to still have privacy is by adding a username and password to the system for those who need it. The information will still be available, but there was something protecting that data.

  ```



---
(Did you remember to add your name at the top of this document?)
