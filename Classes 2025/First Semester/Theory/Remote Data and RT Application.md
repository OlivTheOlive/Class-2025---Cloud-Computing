[BrightSpace](https://brightspace.algonquincollege.com/d2l/le/content/825152/Home)

#### Week 3
REST (*<u>Representational</u>* State Transfer)
- In REST, resources (like a book, user, or order) are represented in different formats.  
- Common representation: JSON, but it could also be XML, HTML, or plain text.  
- Example: A “Book” resource can be represented as JSON when returned from an API.
REST (Representational *<u>State</u>* Transfer)
- “State” refers to the current information about a resource at a given time. 
- Example: A book’s title, author, and availability are its state.
REST (Representational State <u>Transfer</u>)
- REST is about transferring these resource representations between client and server over HTTP.  
- The client requests the current state, and the server transfers it
#### Week 4
###### Introduction to GraphQL  
- GraphQL Core Idea: Clients specify the data they need, and the server responds with only that data.
- GraphQL vs. REST: REST provides fixed data shapes through many endpoints, while GraphQL offers flexible queries through a single endpoint.
- GraphQL Analogy: Similar to ordering from a menu where you choose exactly what you want.
###### GraphQL
- **GraphQL Server Role:** Acts as an intermediary between clients and data sources.
	-  Acts as a server for the frontend, receiving queries and fetching data.
- **Client-Server Interaction:** Clients send queries to a single endpoint, and the server fetches data from various sources.
- **Server Functionality:** Translates client queries into data retrieval actions.
- **Data Retrieval:** GraphQL behaves like a client, making requests to various data sources like databases, REST APIs, or microservices.
- **Abstraction Layer:** Shields the frontend from backend complexities, providing a unified API.
- A query language for APIs.
GraphQL allows the client to define the structure of the response data. This flexibility eliminates the overfetching and underfetching issues found in REST.
###### Why GraphQL
- Graph Definition: A graph is a data structure consisting of nodes and edges.
- Nodes: Represent entities such as users, posts, or comments.
- Edges: Define the relationships between entities, like a user creating a post.
GraphQL queries data graphs, not relational databases.




