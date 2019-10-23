# presto-go-sql
This project allows you to have easy access  to your different datasources like mysql,hive.
###step 1: config your presto url.
###step 2: pass the sql you want to execute.
###step 3: return the query result in json format.

For example,we have presto catalog mysql,schema test and table Persons: 

PersonID	LastName	FirstName	Address	                            City
1	        White	    Clover	    305 - 14th Ave. S. Suite 3B	        Seattle
2	        Wilman	    Kala	    Keskuskatu 45	                    Helsinki

we pass sql[select * from mysql.test.Persons limit 10] and get the result:

[{"address":"305 - 14th Ave. S. Suite 3B","city":"Seattle","firstname":"Clover","lastname":"White","personid":1},
{"address":"Keskuskatu 45","city":"Helsinki","firstname":"Kala","lastname":"Wilman","personid":2}]
