# What is an API?

A set of rules outlining how you should communicate with other software systems.

# What is REST

Representational State Transfer (REST) is a software architecture that imposes conditions on how an API should work.

### Uses and benefits

- Can be used in large scale secure and high performance communications
- Easily implemented and modified

### Naming

- REST APIs - pretty much applies only for APIs
- RESTful web services
- RESTful APIs -

# Principles of REST

### Uniform interface

Fundamental to design of any RESTful webservice. It indicates that the server transfers information in a standard
format. The formatted resource is called a representation in REST. This format can be different from the internal
representation of the resource on the server application.

#### Architectural constraints

1. Requests should identify resources. They do so by using a uniform resource identifier.
2. Clients have enough information in the resource representation to modify or delete the resource if they want to. The
   server meets this condition by sending metadata that describes the resource further.
3. Clients receive information about how to process the representation further. The server achieves this by sending
   self-descriptive messages that contain metadata about how the client can best use them.
4. Clients receive information about all other related resources they need to complete a task. The server achieves this
   by sending hyperlinks in the representation so that clients can dynamically discover more resources.

### Statelessness

In REST architecture, statelessness refers to a communication method in which the server completes every client request
independently of all previous requests. Clients can request resources in any order, and every request is stateless or
isolated from other requests. This REST API design constraint implies that the server can completely understand and
fulfill the request every time.

### Layered system

In a layered system architecture, the client can connect to other authorized intermediaries between the client and
server, and it will still receive responses from the server. Servers can also pass on requests to other servers. You can
design your RESTful web service to run on several servers with multiple layers such as security, application, and
business logic, working together to fulfill client requests. These layers remain invisible to the client.

### Cacheability

RESTful web services support caching, which is the process of storing some responses on the client or on an intermediary
to improve server response time. For example, suppose that you visit a website that has common header and footer images
on every page. Every time you visit a new website page, the server must resend the same images. To avoid this, the
client caches or stores these images after the first response and then uses the images directly from the cache. RESTful
web services control caching by using API responses that define themselves as cacheable or noncacheable.

### Code on demand

In REST architectural style, servers can temporarily extend or customize client functionality by transferring software
programming code to the client. For example, when you fill a registration form on any website, your browser immediately
highlights any mistakes you make, such as incorrect phone numbers. It can do this because of the code sent by the
server.

# Benefits of RESTful APIs

### Scalability

Systems that implement REST APIs can scale efficiently because REST optimizes client-server interactions. Statelessness
removes server load because the server does not have to retain past client request information. Well-managed caching
partially or completely eliminates some client-server interactions. All these features support scalability without
causing communication bottlenecks that reduce performance.

### Flexibility

RESTful web services support total client-server separation. They simplify and decouple various server components so
that each part can evolve independently. Platform or technology changes at the server application do not affect the
client application. The ability to layer application functions increases flexibility even further. For example,
developers can make changes to the database layer without rewriting the application logic.

### Independence

REST APIs are independent of the technology used. You can write both client and server applications in various
programming languages without affecting the API design. You can also change the underlying technology on either side
without affecting the communication.

# Python APIs

We can use Python to make APIs because Python supports working with XML and JSON, which are the building blocks for APIs

# RESTful API request

1. URI (Unique Resource Identifier)
2. Method
    - GET
        - Used to access resources that are located at the specified URL on the server.
    - POST
        - Used to send data to the server.
    - PUT
        - Used to update existing resources on the server.
    - DELETE
        - Used to request to remove the resource.
3. HTTP Header 
   - Request headers are the metadata exchanged between the client and server.
      - Data
        - Must contain one of the http methods (Get,Post, Put etc.)
      - Parameters
        - Path to specify URL details
        - Query parameters to request additional data about the resource
        - Cookie parameters to identify users