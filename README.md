# Neo4j – Graph DB

##  What is Graph DB

- They’re not visual graph and charts. 
- Data is represented as nodes, which are connected by edges, or relationships. 
- Each node and edge can also have properties, which store additional information about the data. 
- The graph model is a natural fit for data with complex relationships, such as social networks, supply chains, and biological networks.
- Graph databases, though just around a decade old, are witnessing a wide adoption in recent years, in the insight-hungry business world.
- Relationships are first-class citizens, and queries can traverse relationships directly.
- <img src="https://github.com/ImranAzizPC/neo4j/assets/133036892/723cb200-b7f1-4104-b198-58efe0fd972b" width="500">

## How it differs from Relational DB model

- A relational database is based on the relational model, which stores data in tables with rows and columns. 
- In a relational database, relationships between data are typically represented using foreign keys and join operations. 
- RDBMs are very good at handling structured data with a fixed schema, they can become slow and complex when dealing with highly interconnected data.
- The relational databases withstood the test of time, and are here to stay at least for the foreseeable future, even if not forever.
 <graphic>

Factor | Graph | Relational Database
--- | --- | --- 
Storage approach | Entities and Relationships are stored as Nodes and Edges respectively | Data is stored in tables as rows and columns. Joins are created between tables for fast querying. The relationships between the columns of a table are inferred, but never stored separately.
Schema | Schema-free. Unstructured.	| Rigid schema. Data Structure and format are pre-defined.
Purpose	| Solely for uncovering hidden insights. Doesn’t serve operational purposes. | Serves both operational and analytics purposes
Performance | Blazing fast even for large sets of data | Relatively slower than Graph DBs
Maintenance	| A lot easy, as they are schema-free | Difficult and often cumbersome, as minor changes could affect the entire structure 
    

In Graph DBs like Neo4J, Queries can traverse relationships directly. This allows for faster and more efficient traversal of relationships and enables complex queries that can be challenging or impossible in a relational database.

Basically graph databases and relational databases have different use cases. Graph databases are ideal for applications that involve highly interconnected data and complex queries, such as social networks, recommendation engines, and fraud detection. Relational databases are well-suited for applications that involve structured data with a fixed schema, such as accounting systems and inventory management.
    
    
## Neo4J
    
Neo4j is a popular graph database management system that is designed to store and manage highly connected data. At the core of the Neo4j graph model are three primary components: nodes, relationships, and properties.

### 1. Nodes:

A node is a fundamental unit of data in the Neo4j graph model. It represents a single entity or object in the system, such as a person, a company, or a product. A node is identified by a unique identifier called a node ID or "label." Nodes can also have one or more properties associated with them that provide additional information about the node. For example, a person node might have properties such as "name," "age," "gender," and "address."

### 2. Relationships:

Relationships are connections between nodes in the Neo4j graph model. They represent how two nodes are related to each other. Relationships are always directed, which means that they have a start node and an end node. A relationship is identified by a unique identifier called a relationship type or "label." Relationships can also have one or more properties associated with them that provide additional information about the relationship. For example, a "friend" relationship between two person nodes might have properties such as "date added," "strength," and "frequency of communication."

### 3. Properties:

Properties are key-value pairs that are associated with nodes and relationships in the Neo4j graph model. They provide additional information about the node or relationship they are associated with. Properties can be any data type, such as strings, numbers, or dates. Properties are stored in the database and can be indexed for fast querying. For example, a person node might have properties such as "name," "age," and "address," while a relationship might have properties such as "date added," "strength," and "frequency of communication."

Together, nodes, relationships, and properties provide a flexible and powerful way to model highly connected data in Neo4j. By using these core components, developers can build sophisticated graph-based applications that are highly scalable and performant.
    
## Overview of the Cypher query language and its use in Neo4j.

## Key features of Neo4j: 
- Explanation of the key features of Neo4j, such as its support for ACID transactions, high scalability and high availability, and its flexible data model.
- Overview of the different editions of Neo4j including the Community edition, the Enterprise edition, and the Aura cloud-based offering.

## Use cases for Neo4j: 
- Examples of how Neo4j is used in real-world scenarios, such as social networks, recommendation engines, fraud detection, and identity and access management.
- Explanation of how Neo4j is used in different industries, including healthcare, finance, retail, and logistics.

## Code demo
