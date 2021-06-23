# exm


--1.	Create the tables for above scenario with correct relationship
-- database create
create database sell_onion
--table create
create table sellerinfo(
SellerID varchar(25) primary key,
sellername varchar(22) not null,
storeid int not null,
)
--data insert
insert into sellerinfo(SellerID,sellername,storeid)
values('193-35-2926','Abul',1011),
('19','Babul',1021),('january','Karina',2002),('2-1-2002','Rahim',1011)
--data show 
select*from sellerinfo
--table create
create table InvoiceInfo(
InvoiceId varchar(25) primary key,
OnionType varchar(25) not null,
Price int,
QtyKG float not null,
InvoiceDate varchar(26) not null,
SellerID varchar(25) Foreign key REFERENCES sellerinfo (SellerID)
);



.........................

--1.	Create the tables for above scenario with correct relationship
-- database create
create database sell_onion
--table create
create table sellerinfo(
SellerID int primary key,
sellername varchar(22) not null,
storeid int not null,
)
--data insert
insert into sellerinfo(SellerID,sellername,storeid)
values(11,'Abul',1011),
(13,'Babul',1021),(11,'Karina',2002),(24,'Rahim',1011)
--data show 
select*from sellerinfo
--table create
create table InvoiceInfo(
InvoiceId varchar(25) primary key,
OnionType varchar(25) not null,
Price int,
QtyKG float not null,
InvoiceDate varchar(26) not null,
SellerID int Foreign key REFERENCES sellerinfo (SellerID)
);
--data insert
insert into InvoiceInfo(InvoiceId,OnionType,Price,QtyKG,InvoiceDate,SellerID)
values('O112','Egypt',40,6,'11 Dec 2019','11'),
('O223','Bangla',130,2.5,'10 Dec 2019','13'),
('O334','India',90,3,'8 Dec 2019','11'),
('O445','Bangla',130,2,'10 Dec 2019','24')



--1.	Create the tables for above scenario with correct relationship
-- database create
create database sell_onion
--table create
create table sellerinfo(
SellerID int primary key,
sellername varchar(22) not null,
storeid int not null,
)
--data insert
insert into sellerinfo(SellerID,sellername,storeid)
values(2926,'Abul',1011),
(19,'Babul',1021),(1,'Karina',2002),(2,'Rahim',1011)
--data show 
select*from sellerinfo
--table create
create table InvoiceInfo(
InvoiceId varchar(25) primary key,
OnionType varchar(25) not null,
Price int,
QtyKG float not null,
InvoiceDate varchar(26) not null,
SellerID int Foreign key REFERENCES sellerinfo (SellerID)
)
--data insert
insert into InvoiceInfo(InvoiceId,OnionType,Price,QtyKG,InvoiceDate,SellerID)
values('O112','Egypt',40,6,'11 Dec 2019',2926),
('O223','Bangla',130,2.5,'10 Dec 2019',19),
('O334','India',90,3,'8 Dec 2019',1),
('O445','Bangla',130,2,'10 Dec 2019',2)
--data show 
select*from InvoiceInfo
select*from sellerinfo
--3.	Show the name of Seller who works in same shop.
SELECT*FROM sellerinfo
      WHERE sellername = '';
--4.	Find the Onion which has highest price than all others.
select max(Price) as highest_price from InvoiceInfo


--3.	Show the name of Seller who works in same shop.
SELECT*FROM sellerinfo
      WHERE sellername = '';
--4.	Find the Onion which has highest price than all others.
select max (price) as highest_price from InvoiceInfo;
--5.	Show the information of seller who sold Indian onion.
select * from InvoiceInfo where OnionType = 'India';
--6.	Find the store id which have more than one employee.

--7.	Show the price of onion which is more than 40 taka per kg
select * from InvoiceInfo where Price > 40
--8.	Find which seller earned maximum amount selling onion.
--9.	Find the invoice info which price is in between 40and 190.
select * from InvoiceInfo where price = 190 or price =40;



....................................


--3.	Show the name of Seller who works in same shop.
SELECT*FROM sellerinfo
      WHERE sellername = '';
--4.	Find the Onion which has highest price than all others.
select max (price) as highest_price from InvoiceInfo;
--5.	Show the information of seller who sold Indian onion.
select * from InvoiceInfo where OnionType = 'India';
--6.	Find the store id which have more than one employee.

--7.	Show the price of onion which is more than 40 taka per kg
select * from InvoiceInfo where Price > 40
--8.	Find which seller earned maximum amount selling onion.
--9.	Find the invoice info which price is in between 40and 190.
select * from InvoiceInfo where price = 190 or price =40;


.............................


--1.	Create the tables for above scenario with correct relationship
-- database create
create database sell_onion
--table create
create table sellerinfo(
SellerID int primary key,
sellername varchar(22) not null,
storeid int not null,
)
--data insert
insert into sellerinfo(SellerID,sellername,storeid)
values(2926,'Abul',1011),
(19,'Babul',1021),(1,'Karina',2002),(2,'Rahim',1011);
--data show 
select*from sellerinfo
--table create
create table InvoiceInfo(
InvoiceId varchar(25) primary key,
OnionType varchar(25) not null,
Price int,
QtyKG float not null,
InvoiceDate varchar(26) not null,
SellerID int Foreign key REFERENCES sellerinfo (SellerID)
)
--data insert
insert into InvoiceInfo(InvoiceId,OnionType,Price,QtyKG,InvoiceDate,SellerID)
values('O112','Egypt',40,6,'11 Dec 2019',2926),
('O223','Bangla',130,2.5,'10 Dec 2019',19),
('O334','India',90,3,'8 Dec 2019',1),
('O445','Bangla',130,2,'10 Dec 2019',2)
--data show 
select*from InvoiceInfo
select*from sellerinfo
--3.	Show the name of Seller who works in same shop.
select sellername from sellerinfo where SellerID = 1011;
--4.	Find the Onion which has highest price than all others.
select max (price) as highest_price from InvoiceInfo;
--5.	Show the information of seller who sold Indian onion.
select * from InvoiceInfo where OnionType = 'India';

--6.	Find the store id which have more than one employee.
select count (SellerID) from sellerinfo;
--7.	Show the price of onion which is more than 40 taka per kg
select * from InvoiceInfo where Price > 40
--8.	Find which seller earned maximum amount selling onion.
SELECT* FROM invoiceinfo WHERE  price>=130;
--9.	Find the invoice info which price is in between 40and 190.
select * from InvoiceInfo where price = 190 or price =40;
--10.	Find the sellers whose name contains h in 3rd position
SELECT sellername FROM sellerinfo WHERE sellername LIKE '__h%';







...............................................................................................................................................................................................

create database sell_onion;
DROP DATABASE databasename;



........................................................................................


create database sell_onion;
DROP DATABASE sell_onion;



create table sellerinfo(
SellerID int primary key,
sellername varchar(22) not null,
storeid int not null,
)
DROP table sellerinfo;

......................................................................................................


create database StudentManagementSystem
-- create student table
CREATE TABLE Student (
ID int PRIMARY KEY,
LastName varchar(255) NOT NULL,
FirstName varchar(255),
Age int
);
-- drop student table 
drop TABLE Student
--add column
alter table student
add addresses varchar(233)
select * from student
--attribute data type change
ALTER TABLE student
ALTER COLUMN age varchar(22)
--attribute data type change
ALTER TABLE student
ALTER COLUMN age int
---drop column
alter table student
drop column age
select * from student
---add column
alter table student
add age int
select * from student
-- insert data
insert into student
values(13,'Tahsinul','Islam','Dhaka',19),
(14,'Ahsanul','Islam','Azimpur',20)
select * from student

-- create admin table
CREATE TABLE Admin (
ID int FOREIGN KEY REFERENCES Student(ID),
FullName varchar(255) NOT NULL,
Registration date not null,
);
-- insert data
insert into Admin
values(11,'Rahin','2020-02-02'),(12,'Rana','2020-03-03'),
(13,'Ratul','2020-04-04'),(14,'Sakib','2020-05-05');
select * from Admin

select * from Student
select * from Admin

-- create course table
CREATE TABLE course (
LabCourseCode int,
LabCourse varchar(233),
TheoryCourseCode int,
TheoryCource varchar(233),
);
-- insert data
insert into course
values (1,'OOD',2,'English'),(3,'OOP',4,'ComputerArchitecture'),
(5,'DatabaseSystemslab',6,'DatabaseSystems');
select * from course






















......................................................................................................................

1. https://drive.google.com/file/d/1n0E0EvsKZjscA1OdlbCrtEg1TTzcNcTo/view
2. https://docs.google.com/document/d/1wfn-WjcpClgYDAkKEtgvH0IWgXuZM9l8CPbc8sdE38s/edit       amd      https://docs.google.com/document/d/1TcXf9XViJw3lfMrPz3YItU-k9ECa5ATqXzCUclwZeDk/edit
3. *** https://www.w3schools.com/sql/sql_drop_db.asp
4. https://docs.google.com/document/d/1TF7SzA7cLFMkzTThJZBmiDjaAto4EyAi/edit

........................................




create database StudentManagementSystem
-- create student table
CREATE TABLE Student (
ID int PRIMARY KEY,
LastName varchar(255) NOT NULL,
FirstName varchar(255),
Age int
);
-- drop student table 
drop TABLE Student
--add column
alter table student
add addresses varchar(233)
select * from student
--attribute data type change
ALTER TABLE student
ALTER COLUMN age varchar(22)
--attribute data type change
ALTER TABLE student
ALTER COLUMN age int
---drop column
alter table student
drop column age
select * from student
---add column
alter table student
add age int
select * from student
-- insert data
insert into student(ID,LastName,FirstName,Age)
values(13,'Tahsinul','Islam','Dhaka',19),
(14,'Ahsanul','Islam','Azimpur',20)
select * from student

-- create admin table
CREATE TABLE Admin (
ID int FOREIGN KEY REFERENCES Student(ID),
FullName varchar(255) NOT NULL,
Registration date not null,
);
-- insert data
insert into Admin
values(11,'Rahin','2020-02-02'),(12,'Rana','2020-03-03'),
(13,'Ratul','2020-04-04'),(14,'Sakib','2020-05-05');
select * from Admin

select * from Student
select * from Admin

-- create course table
CREATE TABLE course (
LabCourseCode int,
LabCourse varchar(233),
TheoryCourseCode int,
TheoryCource varchar(233),
);
-- insert data
insert into course
values (1,'OOD',2,'English'),(3,'OOP',4,'ComputerArchitecture'),
(5,'DatabaseSystemslab',6,'DatabaseSystems');
select * from course

select * from student
select * from Admin
select * from course

--where
--find the student information whose age is greater than 20
select *from student where age>20

----find the student lasname and address whose age is greater than 20
select lastname, addresses from student where age>20

--find the admin information whose name is Rana
select*from admin where FullName='Rana'

--and, or, not
--find out lastname of those student whose age is greater than 20 and he /she must be from
--dhanmondi
select lastname from student where age>20 and addresses='Dhanmondi'

--find out lastname of those student whose age is either greater than 20 or he /she from
--dhanmondi
select lastname
from student
where age>20 or addresses='Dhanmondi'
--find out lastname of those student whose age is greater than 20 but he is not from
--dhanmondi
select lastname, addresses, age
from student
where age>20 and not addresses = 'Dhanmondi'

--order by
--list the student information according to their age
select * from student order by age asc

--NULL
--find those student whose address is not available
select * from student where addresses is NULL

--find those student whose address is available
select * from student where addresses is NOt NULL

--update
--update Tahsinul address BOgura
update student set addresses='Bogura' where LastName='Tahsinul'

select*from student

--update Tahsinul address from Bogura to dhanmondi
update student set addresses='Dhanmondi'where lastname='Tahsinul'

select*from student



select * from student
select * from Admin
select * from course

--add column
alter table course add ID int FOREIGN KEY REFERENCES student(ID)


-- insert data
insert into course
values (7,'Bangla',8,'Robotics',11),
(9,'SDLC',10,'SoftwareArchitecture',12);

select * from course

--extraction from two table
-- who take SoftwareArchitecture course
 select firstName from course,student 
 where TheoryCource='SoftwareArchitecture' and course.id=student.id

 --aggregate function
--min, max, avg, sum, count
--min
--Find out lowest age
select min(age)
from student
--max
--Find out highest age
select max(age)
from student

--find out number of unique addresses present in the student table
select count(distinct addresses) as totalcountry
from student

--like
--Find out those Admin whose name start with r
select FullName from Admin where FullName like 'r%'

--Find out those Admin whose name ends with r
select FullName from Admin where FullName like '%r'

--in any position r
select FullName from Admin where FullName like '%r%'

--2nd position a
select FullName from Admin where FullName like '_a%'

--in
SELECT lastname, addresses
FROM student
WHERE addresses IN ('Dhanmondi','azimpur','dinajpur' );

select * from student
select * from Admin
select * from course

--selects all name with a age between 10 and 20
SELECT * FROM student
WHERE age BETWEEN 10 AND 20;

--group By
--find out the number of student for each address
select count(Lastname) , addresses
from student group by addresses

select count(Lastname) as NumberOfStudent, addresses
from student group by addresses

--find out highest age from each address
select max(distinct age) as HighestAge, addresses from student group by addresses

--having

--find out highest age from each address where age must be greater than 20
select max(distinct age) as highestage, addresses from student group by addresses
having max(distinct age) > 20

--join
-- left outer join - right outer join
--inner join

-- who take SoftwareArchitecture course
select student.lastname from course JOIN student 
ON course.TheoryCource='SoftwareArchitecture' and course.id=student.id

--inner join
select * from course INNER JOIN student 
ON course.TheoryCource='SoftwareArchitecture' and course.id=student.id

--LEFT JOIN
select * from course LEFT JOIN student 
ON course.TheoryCource='SoftwareArchitecture' and course.id=student.id

--RIGHT JOIN
select * from course RIGHT JOIN student 
ON course.TheoryCource='SoftwareArchitecture' and course.id=student.id

--FULL OUTER JOIN
select * from course FULL OUTER JOIN student 
ON course.TheoryCource='SoftwareArchitecture' and course.id=student.id

--left outer join 
select * from course left outer join  student 
ON course.TheoryCource='SoftwareArchitecture' and course.id=student.id

--right outer join
select * from course right outer join  student 
ON course.TheoryCource='SoftwareArchitecture' and course.id=student.id

-- find information who take Robotics course
select * from course  join  student 
ON course.TheoryCource='Robotics' and course.id=student.id

--sub queries
--find student information highest age 
select * from student where age = (select max (age) from student)

--view

CREATE  VIEW b as
select firstname from student where addresses = 'dhanmondi'

DROP VIEW b

DROP database StudentManagementSystem

DROP TABLE course
























..........................................................................................................................................................................






1.https://drive.google.com/file/d/1n0E0EvsKZjscA1OdlbCrtEg1TTzcNcTo/view
2.https://docs.google.com/document/d/1wfn-WjcpClgYDAkKEtgvH0IWgXuZM9l8CPbc8sdE38s/edit
3.https://docs.google.com/document/d/1TcXf9XViJw3lfMrPz3YItU-k9ECa5ATqXzCUclwZeDk/edit
4.https://www.w3schools.com/sql/sql_and_or.asp
5.*** https://www.youtube.com/playlist?list=PLgH5QX0i9K3qLcx9DvVDWmNJ7riPvxzCD
6.https://drive.google.com/drive/u/1/folders/1QINLf1Ju4y4eBKS6SWeIJMLLFNPt5hMZ

*** EXPERIMENT : https://docs.google.com/document/d/1TF7SzA7cLFMkzTThJZBmiDjaAto4EyAi/edit


1.https://www.youtube.com/watch?v=kBdlM6hNDAE&list=PLxCzCOWd7aiFAN6I8CuViBuCdJgiOkT2Y
2.https://www.youtube.com/watch?v=JtmfAGM4pfc
3.https://www.youtube.com/watch?v=_yog7h4BokQ
4.https://www.youtube.com/watch?v=9lLpe_detTY
5.https://www.youtube.com/watch?v=apNmMWgFFRg
6.Database  state Transaction: https://www.youtube.com/results?search_query=Database++state+Transaction
7.https://www.youtube.com/watch?v=xoTyrdT9SZI
8.SQL Server - SubQueries and Correlated SubQueries : https://www.youtube.com/watch?v=BKpO6CpEe50&t=798s



.......................................

Database Normalization - 1NF, 2NF, 3NF, BCNF, 4NF and 5NF : https://drive.google.com/file/d/1jCbPCtidQgGXZ83H6rN10qf6T0hrJc72/view
1.https://www.youtube.com/playlist?list=PLLGlmW7jT-nTr1ory9o2MgsOmmx2w8FB3
2.https://www.youtube.com/playlist?list=PLdo5W4Nhv31b33kF46f9aFjoJPOkdlsRc
3.https://www.youtube.com/playlist?list=PLxCzCOWd7aiFAN6I8CuViBuCdJgiOkT2Y
