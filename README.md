# SPARK TUTORIAL

### INTRODUCTION TO APACHE SPARK
Apache spark is a fast, in-memory data processing engine which allows data workers to effiently execute streaming, machine learning or SQL workloads that require fast iteractive access to datasets.

##### SPEED
It is a very critical aspect in processing large data sets as it means the difference between exploring data interactively and waiting minutes or hours.
- Run computations in memory
- Apache Spark has an advanced DAG execution engine that supports acyclic data flow and in-memory computing.
- Enables applications in Hadoop clusters to run up to 100 times faster in memory and 10 times faster even when running on disk than MapReduce.

##### GENERALITY
- A general programming model that enables developers to write an application by composing arbitrary operators.
- Spark makes it easy to combine different processing models seamlessly in the same application.
- Example:
  - Data classification through Spark machine learning library.
  - Streaming data through source via Spark Streamming.
  - Querying the resulting data in real time through Spark SQL.


### ENVIRONMENT NOTES
- Spark is built on top of the Scala programming language which will be compiled to Java bytecode.
- Our Spark examples use Java 8 features.


Using IntelliJ idea, just go to the folder where the code is cloned, then run
- gradlew idea

### RDD: Resilient Distributed Dataset
RDD is a core object that we will be using when developing with Spark applications.

##### What is a dataset?
A dataset is basically a collection of data; it can be a list of strings, a list of integers or even a number of rows in a relational database.
- RDDs can contain any types of objects, including user-defined classes.
- An RDD is simply a capsulation around a very large dataset. In Spark all work is expressed as either creating new RDDs, transforming existing RDDs, or calling operations on RDDs to compute a result.
- Under the hood, Spark will automatically distribute the data contained in RDDs across your cluster and parallelize the operations you perform on them.

##### What can we do with RDDs?
RDDs offered two types of operations TRANSFORMATIONS and ACTIONS.
###### TRANSFORMATIONS.
- Apply some functions to the data in RDD to create a new RDD.
- One of the most common transformations is ```filter``` which will return a new RDD with a subset of the data in the original RDD.
```java
JavaRDD<String> lines = sc.textFile("in/uppercase.text");
JavaRDD<String> linesWithFriday = lines.filter(line -> line.contains("Friday"));
```
###### ACTIONS.
- Compute a result based on an RDD.
- One of the most popular Actions is ```first```, which returns the first element in an RDD.
```java
JavaRDD<String> lines = sc.textFile("in/uppercase.text");
String firstLine = lines.first();
```
##### Spark RDD general Workflow
- Generate initial RDDs from external data.
- Apply transformations.
- Launch actions.





















