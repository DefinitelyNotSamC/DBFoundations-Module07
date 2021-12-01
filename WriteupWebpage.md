Sam Chen <br>
November 30, 2021 <br>
IT FDN 130 A <br>
Assignment 07

# SQL User Defined Functions

## Introduction

This paper will discuss the use case for SQL User Defined Functions (UDFs), and explore the most common types of functions: Scalar, Inline, and Multi-Statement functions.

## When to Use a UDF

In writing code, it is widely considered a best practice to avoid redundancy by replicating a block of code multiple times. Therefore, when the same set of functions need to be performed multiple times within a query, the developer can utilize UDFs to avoid this redundant code. UDFs achieve this by storing a desired set of functions, then passing an input (or a set of inputs) through it multiple times, when called throughout the query.

## Types of Functions

The three most common types of UDFs are Scalar, Inline, and Multi-Statement functions, which differ in their inputs, outputs, and method of processing data.
Beginning with the simplest of the three, a Scalar function can accept any number of inputs (including zero), but will always return a single value. As a result of these limitations, Scalar functions are typically used to perform computations, or look up specific values from tables. <br>

Next, an Inline function can accept any number of inputs, and will returns a data table derived from a single SELECT statement. While input variables are optional, they can be used to make the function more dynamic, and is a common reason why an Inline function may be selected over creating a view. <br>

Finally, Multi-Statement functions can be thought of as extended versions of Inline functions. In addition to returning a table, these functions can utilize Transact SQL (T-SQL) statements to perform operations like inserting rows, retrieving multiple rows of data, etc. Multi-Statement functions are used whenever developers need to store more complex operations in a function.[1]

## Conclusion

To conclude, this paper has explored what UDFs are able to accomplish within SQL queries, and the three most common function types: Scalar, Inline, and Multi-Statement functions. While these functions share a similarity in that they all take inputs, process data, and return outputs, they vary significantly in how they do so: the types of inputs, what type of data they commonly process, and what they return.

<br>

### Reference

[1] External Link. T P Reddy, “How to Create Scalar, Inline and Multi-Statement Table Valued User Defined Functions in SQL Server,” Microsoft Power BI Kingdom. 2021-01-12, 2021-11-30, https://excelkingdom.blogspot.com/2018/01/how-to-create-scalar-inline-and-multi.html
