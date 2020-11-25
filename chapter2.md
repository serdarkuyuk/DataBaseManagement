# Architecture and Classification of DBMS

# Architecture of DBMS

![](./figures/architecture.png)

## Connection and Security manager

* username, password. login credentials
* multiple process, multi threads
* read versus write access

## DDL compiler

3 DDL (internal, logical, extermanl data model)
* SQL is as DDL
* parse defination, check errors
* after compilation and register to DBMS

## Query processor

* assist retrieval, insertion update or removal data
* query parser, rewriter, otimizer etc

## DML compiler (data manipulation language)

Procedural DML

* how to navigate db
* no query processor
* record at a time

Declarative DML (not prefered) SQL
* what data, what changes
* query processor
* set at a time

## DML Compiler

* impedance mismatch problem

Mapping between java and SQL concepts

* Impedance mismatch solutions

### Query parser and Query rewriter

syntactival semantical correctness

### Query optimzer

* predefined indexes
* number of I/O operations
* CPU processing cost
* execution time
* is key competitive asset of a DBMS

### Query executer

## Storage Manager

### Transaction Manager
supervises execution of db. read and write. ACID properties.
* commit or rollback transactions

### Buffer manager

internal memory, cacheing speedy access.
* data locality: data recently retrieved is likely to be retrieved again
* 80% data is read and 20% is write only

### lock manager
* concurrency control > data integrity at all times
* read and write locks
* avoid conflicts
* locking protocols

### recovery manager
* to undo actions, observes transactions

### DBMS interfaces
* web-base
* commandline
* admin
* network etc

![](./figures/interfaces.png)


# Category of DBMS

## Data model

### Hierarchical DBMS

* tree like
* DML procedural and record oriented
* no query processor
* IMS(IBM)

### Network DBMS

* network
* CODASYL DBMSs
* DML procedural and record oriented
* no query processor

### Relational DBMS

* relational data models
* most populer
* SQL (declarative and set oriented)
* query processor
* strict separation between logical and internal data models (data independence)
* MySQL (Oracle), Oracle DBMS, DB2 (IBM), Microsoft SQL

### Object-Oriented DBMS (OODBMS)
* based upon OO data model
* no impedance mismatch in combination with OO host language
* db4o(open source, Versant) Cache (intersystems) Gemstone
* only successful in niche markets due to their complexity

### Object-Relational DBMS (ORDBMSs)
* called extended relational dbs
* similar OO concepts
* DML is SQL
* oracle DBMS (oracle), db2, Microsoft SQL

### XML DBMSs

* XML data model to store data
* native XML DBMS map the tree structure of an XML to physical storage
* XML-enabled DBMS (oracle IBM DB2)

### NoSQL DBMS (Not Only)

* targeted big and unstructured data
* key-value stores, column-oriented db, graph dbs.
* focus on scalability and ability to cope with irregular or high volatile data structures
* Apache Hadoop, MangoDB, Neo4j

## degree of simultaneous access

* single user vs multi user systems

## architecture

* centralized
* Client server
* n-tier > web servers for web based
* cloud > third party Apache Cassandra and Google BigTable
* Federated > uniform interface to multible underlying data sources
* in-memory DBMs, disk  often used real-time purposes > HANA (SAP)

## Usage

### OLTP Online transaction processing

* focus on managing operational or transactinal data
* lots of simple transaction per unit of time
* DBMS must have good support high value short simple queries

### OLAP Online analytical processing

* opreational tactical or strategical decision.
* limited number of users complex queries
* DBMS should support smaller valuems but complex

### Big data and Analytics

* NoSQL db
* focus on more flexible, even schema-less, database structures
* store unstructured information such as email, text docs, Twitter, Facebook

> key-value db -- couch db
> document base -- MangoDB
> Column base -- Cassandra
> Graph database -- Neo4j

### Multimedia

* Multimedia DBMS for text, images, audio, video, 3d games
* provide content-based query facilities
* need hardware

### Spatial application

* spatial or GIS Geographical Inofrmation Systems

### Sensoring   

* sensor such as biometric from wearables, telematics data

### Mobile

* smartphones, should be online, small footprint, limited processing power
* Oracle light, sql anywhere, sql light, ibm db2 everywhere

### Open Source

* sourceforge.net
* MySQL (oracle) postgre,   
