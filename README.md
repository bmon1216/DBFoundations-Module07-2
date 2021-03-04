SQL Functions
Introduction
	This paper discusses user defined functions and their functionality. I talk about basic uses for user defined functions and show some examples. Lastly, I talk about scalar, inline, and multi-statement functions and their benefits. 
SQL UDF Uses
	User-Defined-Functions serve a handful of purposes. They can act as a check constraint by referencing a column in another table that you can’t otherwise do. See Figure 1.
  Fig.1
The Alter Table statement adds a constraint by checking the function against another table’s column. This is very helpful. Scaler UDF’s can be used to return a single value as an expression.  Using a parameter in this way is super useful. See Figure 2 for a Scaler Function.
 Fig. 2


User defined functions can use parameters which Views cannot. Views can reach the same result using the “where” clause, but I could imagine if you became proficient with functions, you would probably want to stick to the same flow.
  Figure. 3
Scalar, Inline, & Multi-Statement Functions
	Scalar functions can be helpful by creating a new column that is a result of applying a relationship between two previous columns. Multiplying two columns to create an extended price is a common example. See Figure 2 and Figure 4 together.
 Fig.4
An in-line table-valued function just returns a single set of rows. Figure 5 shows the function to sort the table and return only films with the duration requested. 
 Fig.5

 In Figure 6, you can see all the films have a duration of 190+ minutes.
 Fig.6
While a in-line table valued function can only have 1 select statement, a Multi-Statement table valued function can have many or also just 1. With a MSTVF, you can modify and aggregate the output table in the function body. See Figure 7. 
 Fig. 7
“A  multi-statement table-valued function (which I wall call from now on the equally unmemorable MSTVF) is a function which returns a table of data, but only after some additional processing.” (https://www.wiseowl.co.uk/blog/s347/multi-statement.htm)
Summary
 	User defined functions can vary quite but are very useful. Instead of being bound to the basic built-in functions, molding your own function to perfection for a specific use sounds ideal! Scalar, In-line and MSTVF functions are awesome tools to have in your toolbox.
