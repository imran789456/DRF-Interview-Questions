## Core Concepts

### Explain what is REST and RESTful?

* [REST](https://en.wikipedia.org/wiki/Representational_state_transfer) was first introduced by [Roy Fielding](https://en.wikipedia.org/wiki/Roy_Fielding) in 2000.
* REST stands for REpresentational State Transfer. It means that each unique URL is  a represention of some object. it focuses on how state of resource should be transported over HTTP protocol to different clients written in different languages.
* REST is an architectural style.
* It defines several Rules/Guide Lines to develop Web APIs/Web Services very easily in concise way. Hence REST is the most popular Architecture to develop Web Services.

The API which is developed by using REST Architecture is nothing but RESTful API. i.e interface between the user and application where API implements REST Architecture. In  RESTful web service HTTP methods like GET, POST, PUT, PATCH and DELETE can be used to perform CRUD operation.

> REST is basically an architecture where as RESTFul API is an API that implements REST.

### Explain the architectural style for creating any web API based on REST?

The architectural style for creating web api are

* We can use HTTP for client server communication
* We can use XML/JSON to send and receive messages. i.e XML/JSON acts as formatting language.
* Each resource/service can be accessed by a unique URL. This URL acts as the address for the resource/service.
* Stateless communication

### Explain some Key characterics of REST?

The following are various important key characterics of REST

* REST is a stateless and hence SERVER has no state(or session data)
* With a well-applied REST API, the server can be restarted without any impact on 
the client
* Web Services mostly allow
    * GET - To access resources
    * POST - To create resources
    * PUT/PATCH - To update resources
    * DELETE - To delete resources 

## Django Rest Framework

### What is DRF?

Django REST Framework (DRF) is a widely used, full-featured API framework designed for building RESTful APIs with Django. At its core, DRF integrates with Django's core features—models, views, and URLs—making it simple and seamless to create a RESTful API.

### DRF core features

* Serializers
* Views and ViewSets
* Routers
* Authentication and Authorization

### What are serializers?

Serializers are used to convert Django query sets and model instances to and from JSON. Also, before deserializing the data for incoming payloads, serializers validate the shape of the data.

### What are Django REST Framework views and how are they different from Django views?

Django REST Framework views:

* Change incoming requests into Request instances.
* Handle authentication and authorization.
* Perform some sort of action (create, read, update, or delete).
* Return a Response object.

While Django views typically serve up HTML templates, DRF views return a JSON response.

DRF has three different types of views:

* APIView
* Generic View
* ViewSet

### What's the difference between DRF views and ViewSets?

ViewSets allow you to combine related views into a single class. Instead of method handlers, like `.get()` and `.post()`, ViewSets provide actions, like `.list()` and `.create()`.

The advantage of using a ViewSet over a view is that it minimizes the amount of code you need to write and keeps your URLs consistent.

Generic views are meant to handle common use cases without much hassle.

### What is Authentication & Authorization?

Authentication is the process of verifying the identity of a user executing a request, and it doesn't in any way limit access to the API. Authentication can be performed with either a username and password, tokens, or sessions. DRF also supports remote user authentication.

In DRF, authorization has two parts: throttling, and permissions.

Throttling controls the rate of the requests that clients can make to an API. After the rate per user is exceeded, the request will be temporarily denied.

Unlike throttling, which indicates a temporary state, permissions indicate a permanent one. Permissions can control global access (e.g., only authenticated users), access to an endpoint (e.g., only administrators), or even access per object (e.g., only the creator).
