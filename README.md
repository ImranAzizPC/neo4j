# Neo4j – Graph DB

##  What is Graph DB

- They’re not visual graph and charts. 
- Data is represented as nodes, which are connected by edges, or relationships. 
- Graph databases, though just around a decade old, are witnessing a wide adoption in recent years, in the insight-hungry business world.
- Relationships are first-class citizens, and queries can traverse relationships directly.
<img width="1067" alt="Graph DB example" src="https://github.com/ImranAzizPC/neo4j/assets/133036892/b451a3e6-f06a-425c-b558-a380fc0d43bf">


## How it differs from Relational DB model

- The relational databases withstood the test of time, and are here to stay at least for the foreseeable future, even if not forever.

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
Consider a graph database that represents a social network, where users are nodes and relationships represent friendships. Each user has a name and an age, and each friendship has a weight representing the strength of the relationship. Here's how we can use Cypher to query this data:

1. Finding all users in the graph:
```
MATCH (u:User)
RETURN u
```
 
This query uses the MATCH clause to find all nodes in the graph with the label "User" and returns them. The result is a list of all users in the social network.

2. Finding all users who are over 30 years old:
```
MATCH (u:User)
WHERE u.age > 30
RETURN u
```
This query adds a WHERE clause to the previous query to filter the results to only include users who are over 30 years old.

3. Finding the friends of a specific user:
```
MATCH (u:User)-[r:FRIENDS_WITH]->(f:User)
WHERE u.name = 'Alice'
RETURN f
```
 
This query uses the MATCH clause to find all nodes connected to Alice by a FRIENDS_WITH relationship and returns them. The result is a list of all Alice's friends.

4. Finding the strongest friendships in the graph:
```
MATCH (u:User)-[r:FRIENDS_WITH]->(f:User)
RETURN u.name, f.name, r.weight
ORDER BY r.weight DESC
LIMIT 10
```

This query uses the MATCH clause to find all nodes connected by a FRIENDS_WITH relationship and returns the names of the users and the weight of their friendship. The ORDER BY clause sorts the results by weight in descending order, and the LIMIT clause limits the result to the top 10 strongest friendships.

These examples demonstrate how Cypher can be used to query and manipulate data in Neo4j. The syntax is expressive and intuitive, making it easy to work with graph data even for developers who are not familiar with the underlying storage model.

## Key features of Neo4j: 
### Support for ACID transactions:
Neo4j provides full ACID (Atomicity, Consistency, Isolation, Durability) transactional support for all read and write operations. This ensures that data is consistent and reliable, even in the face of concurrent updates and failures.

### High scalability and high availability:
Neo4j is designed for high scalability and high availability, making it suitable for large-scale, mission-critical applications. Neo4j's distributed architecture allows for horizontal scaling across multiple machines, while its clustering capabilities ensure high availability and fault tolerance.

### Flexible data model:
Neo4j's data model is based on a property graph, which allows for flexible and efficient representation of complex, interconnected data. The data model can be easily extended to incorporate new types of data and relationships, making it well-suited for dynamic and evolving data.

### Graph-based querying:
Neo4j provides a powerful graph-based query language called Cypher, which allows users to express complex graph queries in a clear and concise manner. Cypher is designed to be intuitive and easy to use, making it accessible to both developers and non-technical users.

### Rich set of APIs and integrations:
Neo4j provides a wide range of APIs and integrations, including drivers for popular programming languages, a REST API, and support for popular graph visualization tools. This makes it easy to integrate Neo4j with existing applications and toolchains.

Overall, Neo4j's support for ACID transactions, high scalability and high availability, flexible data model, graph-based querying, and rich set of APIs and integrations make it a powerful and versatile platform for managing and analyzing graph data.


## There are different editions of Neo4j 
- Community edition-
- Enterprise edition-
- Aura cloud-based offering.

## Use cases for Neo4j: 
### Social networks:
Neo4j has been used by social networking sites to model and analyze social relationships between users. For example, LinkedIn uses Neo4j to store and retrieve connections between users, as well as to power their "People You May Know" feature.

### Recommendation engines:
Neo4j's flexible data model makes it well-suited for building recommendation engines. For example, Hinge, a dating app, uses Neo4j to match users based on their social connections and interests.

### Fraud detection:
Neo4j has been used to detect fraud in financial transactions. For example, Swisscom, a Swiss telecom company, uses Neo4j to analyze phone call records and identify patterns of fraudulent activity.

### Identity and access management:
Neo4j can be used to manage identity and access control in complex organizations. For example, the Norwegian Ministry of Foreign Affairs uses Neo4j to manage access to their various systems and applications, ensuring that employees have the appropriate levels of access based on their roles and responsibilities.

### Knowledge graphs:
Neo4j's graph-based querying and flexible data model make it an ideal platform for building knowledge graphs. For example, NASA uses Neo4j to model and analyze the relationships between various entities in the space industry, such as spacecraft, launch vehicles, and missions.

## Code demo
