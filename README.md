# db2odata
A Jupyter notebook and magic functions to demonstrate the use of OData RESTful calls to DB2.

## A Brief Introduction to OData

Rather than paraphrase what OData does, here is the official statement from the OData home page:

http://www.odata.org/

>OData (Open Data Protocol) is an ISO/IEC approved, OASIS standard that defines a set of best practices for building and consuming RESTful APIs. OData helps you focus on your business logic while building RESTful APIs without having to worry about the various approaches to define request and response headers, status codes, HTTP methods, URL conventions, media types, payload formats, query options, etc. OData also provides guidance for tracking changes, defining functions/actions for reusable procedures, and sending asynchronous/batch requests.

## Why OData for DB2?

Customers have a wealth of data in their databases (not just DB2) and publishing it to different devices is often fraught with many challenges. DB2 requires the use of client code to communicate between the application and the database itself. Many of APIs that are used are well known: JDBC, .Net, ODBC, OLE-DB, CLI and so on. Most programming languages have some sort of connector that maps from the language syntax to the database driver. When a new language gets developed it always needs this driver code to talk to the database. For instance, the OData Python notebook is communicating to DB2 natively using the ibm_db package. Without some specialized coding, there would be no way to communicate with DB2.

OData tries to remove much of the complexity of communicating with the database. There are no drivers required, no configuration file, nor any administration required on the client that is communicating with the database. All communication is done using RESTful API calls, which are available on all browsers and all operating systems. The calls to the database are replaced with standard POST, GET, DELETE, PUT and PATCH requests.

OData goes one step further and removes the syntactical differences between SQL vendors. The INSERT, DELETE, UPDATE and SELECT statements are coverted to a canonical form that should be interpreted by all vendors. Of course, interoperability depends on how much of the standard a vendor has implemented.

The end result is that an Iphone, Andriod phone, tablet, browser or any application will be able to access the database without having any code installed locally. This simplifies the ability to access the database and makes development considerably easier.

The downside to this approach is that the richness of a particular SQL dialect will not be available through OData. Complex SQL with aggregation functions and moving result windows are not a good candidate to use with OData. However, OData covers much of the query spectrum that traditional applications will use, so it makes it a good choice for agile development.

## OData to DB2 Extension

Writing OData calls to DB2 requires a knowledge of the OData syntax, the RESTful calling sequence, and an understanding of the level of support of OData that DB2 provides. This tutorial will take you through all of the functions that the OData gateway currently provides and show how these calls are implemented. Feel free to use the code and extensions in your own applications.

## OData Gateway Code and developerWorks article
An introduction to the OData gateway is found in the following developerWorks article:

https://www.ibm.com/developerworks/community/blogs/96960515-2ea1-4391-8170-b0515d08e4da/entry/IBM_Data_Server_Gateway_for_OData_Version_1_0_0?lang=en

The code can be obtained through the following link:

https://www-945.ibm.com/support/fixcentral/swg/selectFixes?parent=ibm~Information%2BManagement&product=ibm/Information+Management/IBM+Data+Server+Client+Packages&release=11.1.*&platform=Linux&function=fixId&fixids=*odata*FP001*&includeSupersedes=0&source=fc





