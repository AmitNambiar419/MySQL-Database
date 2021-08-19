# MySQL-Database
Food Ordering system:
Entity sets:(FOOD,CUSTOMER,CART,ORDERS)


Food:
1.id primary key autoincrement
2. name varchar
3.price double
4. avaible_Quantityint
5. type
6.category
------------------

customer:

1.cid {primary key} [type : intauto_increment] assigned for each unique customer.
2.name [type : varchar(30)] represents name of the customer
3.Email [type : varchar(30)] represents email of the customer
4.Pwd [type: varchar(30)] used for saving password of the customer
5.Phnno [type : int(11)] is used for saving phone number of customer
6.Address [type : text] used for saving the address of the customer
----------------------------
cart:

1.Id {primary key} [type : intauto_increment] assigned for each cart
2.Cid foreign key references customer id from the customer table
3.fid foreign key references products table
4.Qty saves all quantities related to products added in cart (default=1)
5.total_per_price,default =0.0 
------------------------------
orders :

1.oid { primary key } [type : intauto_increment] assigned for each order.
2.fid { foreign key references products: pid } .
3.Cid [foreign key references customer: cid]
4.Delivery status [type : tinyint(1)] saves the delivery status whether delivered or pending
5.totalBill default 0.0

FUNCTIONALITY:


Food Table:
----------
Insert data
update data
delete data
Retrive data:
	1. on basis of food name
	2. on basis of food type

Customer Table:
------------
Insert data
update data
delete data
Retrive data:
	1. on basis of Customer name
	2. on basis of email
	3. on basis of 1st letter

Cart Table:
-----------------
1. create a trigger on cart before insert or before update to calulate per price
	example: food price: 100  qnt: 2    totalperPrice=price*qnt=> 100*2+>200
2 insert data
3.updatequntity on basis odcustId

Orders Table:
---------------------
find sum of totalperprice of cart table:
1.insertdata:oid,fid,cid,
2. create trigger to delete data before inserting product in orders table om basis of cid
3.retrive data:
   1. on basis of cid
   2. on basis of date

# create ER diagram for Each.

