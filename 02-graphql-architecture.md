# GraphQL architecture

You can create a new API server with GraphQL in a matter of minutes and it also can integrate with your existing code base because GraphQL is transport- layer agnostic which means you can use it anywhere with any technology.

It is also possible to build a GraphQL API that connects to a database as well as an old or third-party REST API. When a query comes from the client,

GraphQL will decide which resource to use. GraphQL is mostly used by front-end developers because it eliminates most of the shortcomings that front-end developers face with REST. 

There are many client libraries like Apollo that will enable you to use GraphQL on the front-end of your application, these libraries provide all the tools necessary to focus on the important parts of your application rather than dealing with other things. 

## The client side

Using the GraphQL API in the front-end is a great way to develop and implement new functionality for the client. Some features are necessary for almost every application.

- Queries and mutations without constructing HTTP requests.

- Integrate a View-layer.

- Caching.

- Query validation according to the schema.

- Co-locating views and Data dependencies

## The server side

GraphQL is mostly known as a front-end-focused API technology because it helps clients access data in a better way than REST. But the API is implemented on the server-side.

GraphQL provides a better development experience because it handles all the things required for the queries and mutations so that the developers can focus on the more important things. 

GraphQL provides an execution algorithm along with a schema and query language. The algorithm is pretty simple, queries are traversed field by field by executing re solvers for each field. 

GraphQL server provides default providers so that you don't have to provide re-solvers for every single field. If your API supports batched requests we can also make only fetch requests for multiple requests of the same type using GraphQL.
