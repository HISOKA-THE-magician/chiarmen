��#   c h i a r m e n 
 create database nissan;
use nissan;

create table drax(
custom_id int primary key auto_increment,
name varchar (50),
work varchar (50)
);

o
insert into drax (name,work)
values
("starlord","guardian"),
("rocket","racoon"),
("batista","wresteler"),
("gamora","assasian"),
("asian","therapist");

///---- new table----////

create table avengers(
avenger_id int primary key auto_increment,
name varchar (50),
custom_id INT ,
FOREIGN KEY (custom_id) references drax (custom_id)
);

select * from avengers;

insert into avengers (name,custom_id)
values("iron_man",1),
	  ("thor",2),
      ("captain_america",3),
	  ("black_widow",4),
	  ("hulk",5);

alter table avengers 
drop foreign key avengers_ibfk_1;

alter table avengers 
add constraint fk_custom_od 
foreign key (custom_id) references drax (custom_id);


delete from avengers ;

select * from avengers ;

alter table avengers 
auto_increment =1;

delete from drax 
where custom_id = 3;

use nissan;

update avengers 
set avenger_id = 5
where custom_id = 5;

select * from drax;

use nissan;

delete from avengers

where custom_id = 5;

set autocommit = off;

commit;

delete from avengers ;
select * from avengers ;

rollback;


create table test ( 
my_date date , 
my_time time ,
my_datetime datetime 
);

select * from test ;

select *
from avengers inner join drax
on avengers.custom_id =drax.custom_id;

set foreign_key_checks=0;

SELECT * FROM nissan.avengers;

select sumcustom_id
from avengers
group by custom_id ;




 
