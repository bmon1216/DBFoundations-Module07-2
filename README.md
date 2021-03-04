SQL Functions
Introduction
	This paper discusses user defined functions and their functionality. I talk about basic uses for user defined functions and show some examples. Lastly, I talk about scalar, inline, and multi-statement functions and their benefits. 
SQL UDF Uses
	User-Defined-Functions serve a handful of purposes. They can act as a check constraint by referencing a column in another table that you can’t otherwise do. See Figure 1.
  ![image](https://user-images.githubusercontent.com/79563064/109920163-c0556200-7c6e-11eb-91b5-0048edba2e74.png)
![image](https://user-images.githubusercontent.com/79563064/109920182-c5b2ac80-7c6e-11eb-888e-54c55cecbe4b.png)
Fig.1
The Alter Table statement adds a constraint by checking the function against another table’s column. This is very helpful. Scaler UDF’s can be used to return a single value as an expression.  Using a parameter in this way is super useful. See Figure 2 for a Scaler Function.
 ![image](https://user-images.githubusercontent.com/79563064/109920203-cb0ff700-7c6e-11eb-957d-7637c711e887.png)
Fig. 2


User defined functions can use parameters which Views cannot. Views can reach the same result using the “where” clause, but I could imagine if you became proficient with functions, you would probably want to stick to the same flow.
  ![image](https://user-images.githubusercontent.com/79563064/109920218-d2cf9b80-7c6e-11eb-879c-d4afdf137444.png)
![image](https://user-images.githubusercontent.com/79563064/109920227-d6632280-7c6e-11eb-9926-3b4b51ef225d.png)
Figure. 3
Scalar, Inline, & Multi-Statement Functions
	Scalar functions can be helpful by creating a new column that is a result of applying a relationship between two previous columns. Multiplying two columns to create an extended price is a common example. See Figure 2 and Figure 4 together.
 ![image](https://user-images.githubusercontent.com/79563064/109920238-da8f4000-7c6e-11eb-9e8e-d88476d3be94.png)
Fig.4
An in-line table-valued function just returns a single set of rows. Figure 5 shows the function to sort the table and return only films with the duration requested. 
 ![image](https://user-images.githubusercontent.com/79563064/109920248-df53f400-7c6e-11eb-8a93-fa6956e66ce5.png)
Fig.5

 In Figure 6, you can see all the films have a duration of 190+ minutes.
 ![image](https://user-images.githubusercontent.com/79563064/109920272-e67b0200-7c6e-11eb-85ab-b9f6a8fc7d8a.png)
Fig.6
While a in-line table valued function can only have 1 select statement, a Multi-Statement table valued function can have many or also just 1. With a MSTVF, you can modify and aggregate the output table in the function body. See Figure 7. 
 ![image](https://user-images.githubusercontent.com/79563064/109920281-ea0e8900-7c6e-11eb-9a2e-5a01682e8b35.png)
Fig. 7
“A  multi-statement table-valued function (which I wall call from now on the equally unmemorable MSTVF) is a function which returns a table of data, but only after some additional processing.” (https://www.wiseowl.co.uk/blog/s347/multi-statement.htm)
Summary
 	User defined functions can vary quite but are very useful. Instead of being bound to the basic built-in functions, molding your own function to perfection for a specific use sounds ideal! Scalar, In-line and MSTVF functions are awesome tools to have in your toolbox.
