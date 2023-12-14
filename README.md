# Sql-Session-1-
Explored SQL operations on GitHub. Described "customer" table, displayed data using SELECT, showcased filtering, aggregation, and pattern matching. Emphasized code clarity with detailed comments, revealing my adeptness in SQL for potential collaborators or employers.
Describe customer; # describe tables
Select * from customer; # show tables
/* want to look for specific column use */
select First_name, last_name, customer_id
from customer;
use telco;
 select * from billing ; 
 
 select bill_id, amount_due
 from billing;
 
 # how distinct statement work
 
select distinct email # to show unique items in email from customer table
from customer;

select count(distinct email) from customer; # using a count function to calculate number of distinct email
select sum(amount_due) from billing;
Select * from customer where First_name in ("Tore");

# how where clause works
select * from billing
where amount_due>5000;

# use of where with in we check for multiple
# we can use like function to check and using % sign begning is like can begin
#should be these number 
# while we can also do this with %277 its showing ending must be 277 and begining can be anything
select * from customer
where address in("5 Northridge Road","814 Kinsman Lane") and Phone_number like "277%";
select * from customer
where phone_number like ("277%");



select * from billing order by customer_id asc , amount_due desc;
select * from billing limit 10;
