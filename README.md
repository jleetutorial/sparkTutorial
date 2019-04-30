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

RDD: Resiliant Distributed Dataset























