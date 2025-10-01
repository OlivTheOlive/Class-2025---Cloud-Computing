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

#### Week 5
##### Limitation of REST and GraphQL
- **Data Retrieval Mechanism:** Both REST and GraphQL are pull-based, requiring clients to actively request data from the server.
- **Real-time Communication Limitations:** Pull-based systems like REST and GraphQL are not inherently designed for real-time updates, necessitating workarounds like polling or long polling.
- **Persistent Communication Solution:** Enabling persistent full-duplex communication between client and server addresses the limitations of pull-based systems for real-time data exchange.
##### WebSocket
- **WebSocket Protocol:** Provides full-duplex communication over a single TCP connection, enabling real-time data exchange.
- **Data Transmission:** Allows both client and server to send data independently, unlike HTTP’s request-response model.
- **Web-based Protocol:** Designed for web browsers and the internet, integrating with HTTP and using sockets for network communication.
###### Key Features
- **Full-Duplex Communication:** Allows two-way communication, enabling the server to send updates to the client without a client request.
- **Persistent Connection:** Maintains a single connection for continuous communication, reducing the overhead of establishing new connections.
- **Low Latency:** Reduces latency by avoiding repeated HTTP handshakes, making it ideal for real-time applications.
###### Example
- **WebSocket Functionality:** Enables continuous communication between websites and servers without disconnecting after each message.
- **Analogy:** Similar to a text conversation where both parties can send messages back and forth without interruption.
###### Handshake
- **WebSocket Handshake:** The initial phase where the client and server agree to switch from HTTP to WebSocket protocol.
- **Client Request:** The client sends an HTTP request with an “Upgrade” header to initiate the protocol switch.
- **Server Response:** The server responds with an acceptance if it supports WebSockets, leading to a successful handshake and the establishment of a WebSocket connection.
###### Bi-directional Messages
- **WebSocket Communication:** Full-duplex communication over a single, long-lived connection.
- **Ideal Use Cases:** Applications requiring live updates, such as chat applications, live feeds, or gaming.
- **Connection Establishment:** No need to re-establish the connection for each message exchange.

###### Frames
- **WebSocket Data Transmission:** Data is sent in frames, which include headers defining payload length, type, and control information.
- **Frame Types**: Text frames (UTF-8 encoded text), binary frames (binary data), and control frames (protocol-level signalling like “ping” and “close”).
- **Headerless Data Frames:** Unlike HTTP, WebSocket data frames sent after connection establishment do not have headers, reducing overhead and improving efficiency.

###### One Side Closes Channel
- **Connection Termination:** The final phase of a connection where either the client or server decides to close it.
- **Close Frame:** A frame sent by one party to initiate the termination of the connection.
- **Acknowledgement:** The other party acknowledges the close frame, leading to a graceful closure of the connection.

###### Benefits of WebSockets: 
- lower latency
- Efficient Data Transfer

##### Network Bandwidth and Server Load
- **HTTP Polling Drawback:** Wastes network traffic even when there’s no new data.
- **WebSocket Advantage:** Reduces traffic by sending data only when it exists.
- **Benefits of WebSockets:** Lower server costs, faster app performance.
##### Latency and User Experience
- **Polling Drawback:** Polling introduces delay, potentially up to the polling interval, impacting real-time applications.
- **WebSocket Advantage:** WebSockets offer instant communication by pushing messages from server to client as soon as they are available.
- **Real-time Applications:** WebSockets are crucial for applications like chat, trading, gaming, IoT, and notifications, where real-time updates are essential for a smooth user experience.
##### Energy and Device Efficiency
- **Battery Saving:** WebSockets reduce battery drain by eliminating unnecessary HTTP requests from mobile devices.
- **WebSockets Advantage:** Allows devices to remain idle until new information is available, unlike polling with HTTP requests.
- **Impact on Mobile Apps:** Significantly improves battery life, as users are sensitive to battery drain.
##### Scaling to Millions of Users
- **Benefits of WebSockets:** WebSockets enable efficient handling of millions of idle connections, allowing for smooth scaling to millions of users.
- **Impact on System Performance:** WebSockets significantly reduce bandwidth and CPU usage compared to traditional polling, especially with a large user base.
- **User Experience Enhancement:** WebSockets improve responsiveness and enable real-time functionality in applications.
##### Implementing WebSockets
- **WebSocket Protocol Requirement:** Both client and server must implement the WebSockets protocol.
- **Server-Side Implementation:** Modern web frameworks like Node.js and Python (with libraries) support WebSockets.
- **Client-Side Implementation:** Clients can be implemented in various environments (browsers, apps, IoT devices) using different languages and frameworks.






