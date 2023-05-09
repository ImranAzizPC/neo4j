# Neo4j – Graph DB

##  What is Graph DB

    - They’re not visual graph and charts. 
    - Graph databases use nodes to store data entities, and edges to store relationships between entities
    - Data is represented as nodes, which are connected by edges, or relationships. 
    - Each node and edge can also have properties, which store additional information about the data. 
    - The graph model is a natural fit for data with complex relationships, such as social networks, supply chains, and biological networks.
    - Graph databases, though just around a decade old, are witnessing a wide adoption in recent years, in the insight-hungry business world.
    - Relationships are first-class citizens, and queries can traverse relationships directly.
    - <img src="https://github.com/ImranAzizPC/neo4j/assets/133036892/723cb200-b7f1-4104-b198-58efe0fd972b" width="500">

## How it differs from Relational DB model

   - A relational database is based on the relational model, which stores data in tables with rows and columns. 
   - In a relational database, relationships between data are typically represented using foreign keys and join operations. Relationships are infered via schema. 
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
    
    One of the key differences between graph databases and relational databases is the way they handle relationships between data. In a graph database, relationships are first-class citizens, and queries can traverse relationships directly. This allows for faster and more efficient traversal of relationships and enables complex queries that can be challenging or impossible in a relational database.

Another difference is the way graph databases and relational databases handle schema. In a relational database, the schema is fixed and data must conform to that schema. In a graph database, the schema is flexible and can evolve over time as the data changes. This allows for more agile development and better support for dynamic, rapidly changing data.

Finally, graph databases and relational databases have different use cases. Graph databases are ideal for applications that involve highly interconnected data and complex queries, such as social networks, recommendation engines, and fraud detection. Relational databases are well-suited for applications that involve structured data with a fixed schema, such as accounting systems and inventory management.
    
    
3. Understanding the Neo4j graph model: 
   a. Explanation of the core components of the Neo4j graph model including nodes, relationships, and properties.
   c. Overview of the Cypher query language and its use in Neo4j.

4. Key features of Neo4j: 
   a. Explanation of the key features of Neo4j, such as its support for ACID transactions, high scalability and high availability, and its flexible data model.
   b. Overview of the different editions of Neo4j including the Community edition, the Enterprise edition, and the Aura cloud-based offering.

5. Use cases for Neo4j: 
   a. Examples of how Neo4j is used in real-world scenarios, such as social networks, recommendation engines, fraud detection, and identity and access management.
   b. Explanation of how Neo4j is used in different industries, including healthcare, finance, retail, and logistics.

6. Conclusion: 
   a. Recap of the key points of the presentation.
   b. Summary of the benefits of using Neo4j graph database.
   c. Explanation of how to get started with Neo4j.
