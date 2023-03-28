# Advanced Concepts

Fragments help in improving the structure and re-usability of your API. A fragment is a collection of fields for a specific type. You can make fragments to represent information that is related to the address and phone number of a user.

Type definitions can also take arguments like functions. You can pass arguments to fetch data for a specific user or a record that is two years old. 

GraphQL also allows default values for arguments. One of the best feature that GraphQL has is that it lets you send multiple queries in a single request. This causes errors but you can name each query to remove this error.

In GraphQL there are two different kinds of types, Scalar, and Objects. Scalars are concrete units of data GraphQL has five pre-defined scalar types which include strings, integers, floating points, Boolean, and an ID type.

Object types have fields that express the properties of that type and are compostable.

Examples of object types are the User or Post type. You can also create your own custom types if you want.

Enumeration or enums for short are a feature of GraphQL that allows expressing the semantics of a type that has a fixed set of values. 

Interfaces can be used in GraphQL to abstract types. It allows you to specify a set of fields that any concrete type, which implements this interface, needs to have.

In many GraphQL schemas, every type is required to have an id field. Union types can be used to express that a type should be either of a collection of other types.

## Security

GraphQL allows clients to create very complex queries and these queries could be malicious attacks on the server to take it down or still its data.

There are a few ways that we can protect our servers from these types of attacks. The first way to prevent hackers from stealing data from your GraphQL server is by setting up a time limit to how long a query takes to resolve. If it takes more than the allowed time it will be rejected by the server.

Simple to implement and used mostly as a last line of defense Sometimes randomly cutting connections may lead to unstable behavior. Damage could already happen within the allowed time.

Clients can create very complex queries and use them to launch attacks on our servers. We can limit the depth of our queries so that they return only the required data and nothing more. The schema that we define for our servers can help remove this complication.

Using this approach we can sometimes cancel queries which removes load from the server. Depth alone is not enough for large-scale attacks you need to implement multiple security measures to protect your servers.

The depth of a query does not define how complex it is. In a lot of cases, certain fields in our schema are known to be more complex to compute than others. 

Query complexity allows you to define how complex fields can be and restricts them to not accessing more data.

Can be helpful in most attacks on the server but can reject queries before executing them. 

Can be hard to implement and hard to estimate the default complexity and also the mutations can have side effects due to restrictions.

what will we do if the attackers used normal queries but multiple? The answer is throttling our server. You can limit clients to how much time they can access the server and then have a cool down period.

Throttling clients' access to the server-based upon the complexity of their queries is a great way to stay within the limits of the schema.

## Tooling

The ecosystem of GraphQL is rapidly growing because GraphQL makes it easy for developers to create complex solutions easily.

The designers of the schema already know what the schema looks like but how can  clients discover what is accessible through a GraphQL API? We can ask GraphQL for this information by querying the `__schema` meta-field, which is always available on the root type of a Query per the spec.

Introspection is a really powerful tool that dives deep into more details about fields and types available in the introspection schema.

GraphQL Playground is a powerful “GraphQL IDE” for interactively working with a GraphQL API. It features an editor for GraphQL queries, mutations, and subscriptions, equipped with auto-completion and validation as well as a documentation explorer to quickly visualize the structure of a schema (powered by introspection).

It also can display your query history or lets you work with multiple GraphQL APIs side by-side and can seamlessly integrates with your GraphQL config.


