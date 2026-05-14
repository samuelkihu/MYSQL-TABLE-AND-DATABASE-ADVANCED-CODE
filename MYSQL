# MYSQL-TABLE-AND-DATABASE-ADVANCED-CODE
create database prac;
use prac;
set sql_safe_updates=1;
drop database prac;
create table users(
id int auto_increment primary key,
username varchar(100)not null,
email varchar(100) not null,
sam datetime not null,
age int not null,
password varchar(50) unique
);

insert into users(username,email,sam,age,password) values ("sam","adsfhggadsv@sdvghfsg",now(),23,"sfdsahggf");
select*from users;
create table owners(
id int auto_increment primary key,
name varchar(100) not null,
privalege varchar(40) not null,
gender varchar(10) not null,
special_code int unique not null
);

-- data for users table 

insert into users(username,email,age,password) value("samuel kihu","kihusamuel33@gmail.com",12,"samkihu660");
insert into users (username,email,age,password) value("mutanga sam","mutangasam21@gmail.com",44,"mutanga55");
insert into users (username,email,age,password) value("faith wambui","wambuifaith33@gmail.com",66,"wambui433");
insert into users (username,email,age,password) value("wangoi ma","wangoima22@gmail.com",11,"wangoiwa");
insert into users (username,email,age,password) value("mwangi john","johnwangoi12@gmail.com",78,"johny");

insert into owners(name,privalege,gender,special_code) value("samuel kihu","vc","male",367);
insert into owners (name,privalege,gender,special_code) value("mutanga sam","cod","female",455);


select username,email,age from users where age>=20;
select username,email,age from users where age<=20;
select username,email,age from users where username like '%sa%';
select username,email,age from users where username like 'sa%';
delete from users where age>20;
update users set username='wangwan w' where age=12;
select name,gender,privalege,special_code from owners where id=1;
select*from users;
select*from owners;

-- 
create table jobs(
id int auto_increment unique,
job_id varchar(40) not null,
job_name varchar(20),
department varchar(100),
state varchar(50),
user_id int,
FOREIGN KEY (user_id) REFERENCES users(id)
);
insert into jobs (job_id,job_name,department,state,user_id)values("M5TW","SWIPE","CLEANING","PRESENT",5);
insert into jobs (job_id,job_name,department,state,user_id)values("T5MM","WASH","CLEANING","ABSENT",4);
insert into jobs (job_id,job_name,department,state,user_id)values("O99O","SWIPE","CLEANING","PRESENT",3);

select*from jobs;
SELECT users.id,users.username,users.email,users.age,users.password,jobs.state,jobs.job_name,jobs.job_id,jobs.department
FROM jobs
JOIN users ON jobs.user_id = users.id;

create table ranking(
 owners_id int,
 users_id int,
 FOREIGN KEY (owners_id) REFERENCES owners(id),
  FOREIGN KEY (users_id) REFERENCES users(id)
);
insert into ranking value(2,1);
select users.username,owners.name,ranking.owners_id,ranking.owners_id
from ranking
join users on ranking.users_id = users.id;
