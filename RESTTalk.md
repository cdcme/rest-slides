# RESTful APIs

---
= data-x='1000' data-scale='2'
# What's REST?
## REpresentational State Transfer

An **architectural style** for **distributed systems** (like the web).

---
= data-x='1000' data-scale='2'
REST is not a standard, but *does* use standards, like...

---
= data-x='1000' data-scale='2'

 - HTTP
 - URI/URL
 - XML/HTML/GIF/JPEG/PNG (resource representations)
 - text/xml, text/html, image/gif, image/jpeg, etc (MIME types)

---
= data-x='1000' data-scale='2'
# Eight Characteristics of REST APIs

---
= data-x='1000' data-scale='2'
# Uniform Interface
Resources are accessed with a generic interface (e.g., HTTP verbs)

---
= data-x='1000' data-scale='2'
# Stateless
Each request must contain all of the information necessary to understand the request and can't take advantage of any server-side stored context.

---
= data-x='1000' data-scale='2'
# Cacheable
Responses have to be capable of being labeled as cacheable or non-cacheable.

---
= data-x='1000' data-scale='2'
# Client-Server
Consuming components pull representations (pull-based interaction style).

---
= data-x='1000' data-scale='2'
# Layered System
Should be able to accommodate extra layers, like proxy servers, caches, gateways, etc.

---
= data-x='1000' data-scale='2'
# Named Resources
The system has to be built such that every resource has a URL (that resource's name).

---
= data-x='1000' data-scale='2'
# Interconnected Representations
All of the resources are connected via URL

---
= data-x='1000' data-scale='2'
# Code on Demand (optional)
The server can temporarily extend the functionality of the client by sending along executable code.

---
= data-x='1000' data-scale='2'
# Designing an API, step-by-step

---
= data-x='1000' data-scale='2'

 1. What are the entities we want to expose as services (products list, product detail, etc.)?

---
= data-x='1000' data-scale='2'

 2. Create a URL to each resource (http://widgetco.com/products/123)

---
= data-x='1000' data-scale='2'

 3. Which resources can be modified? For these, use POST, PUT, and/or DELETE. For the rest, use GET.

---
= data-x='1000' data-scale='2'

 4. All resources available via GET should be side-effect free (i.e., don't use GET to modify resources...that's a no-no!).

---
= data-x='1000' data-scale='2'

 5. Place links within representations so users can drill down and navigate between resources.

---
= data-x='1000' data-scale='2'
 6. Provide minimal information per response document and let the user get more details via links.

---
= data-x='1000' data-scale='2'

 7. What will the response data's format be (JSON, XML, etc.)?

---
= data-x='1000' data-scale='2'

 8. How will the services be accessed? WSDL? HTML document?

---
= data-x='1000' data-scale='2'
Ta-da! You have a REST API!

---
= data-x='1000' data-scale='2'
# Mapping RESTful URIs to HTTP Verbs

---
= data-x='1000' data-scale='2'
**http://widgetco.com/products/** - GET a list of URIs for all products, PUT a new collection of products (replacing existing products), POST a new product, or DELETE all the products

---
= data-x='1000' data-scale='2'
**http://widgetco.com/products/123** - GET a representation of a specific product, PUT a new product (replacing the existing one) or create one if it doesn't exist, or DELETE this product
**Notice** how POST is not used that often? That's because REST favors PULL-based interactions over the traditional POST-style.

---
= data-x='1000' data-scale='2'
# Some Benefits of the REST Architectural Style

---
= data-x='1000' data-scale='2'
Code *one* API. Then, build as many clients as you want (web, mobile web, phone, tablet) to consume it.

---
= data-x='1000' data-scale='2'
Changes to the API automatically propagate throughout the system.

---
= data-x='1000' data-scale='2'
Not *married* to your client - you can change any or all of them without having to touch the API.

---
= data-x='1000' data-scale='2'
# Some implementation ideas...
1. Build a REST API using [Restify](https://github.com/mcavage/node-restify)
2. Build a website-as-client using [Node](http://nodejs.org/) and [Backbone](http://backbonejs.org/)
3. Build a mobile app using [PhoneGap](http://phonegap.com/)
4. Expose your API for developers
5. Profit!

---
= data-x='1000' data-scale='2'
# References & Links

  - [Architectural Styles and the Design of Network-based Software Architectures](http://www.ics.uci.edu/~fielding/pubs/dissertation/top.htm), by Roy Fielding
  - [REST API Tutorial](http://www.restapitutorial.com/)
  - [How I Explained REST to My Wife](http://tomayko.com/writings/rest-to-my-wife)
  - [Wikipedia's REST Entry](http://en.wikipedia.org/wiki/Representational_state_transfer)
  - [SocialNetifyMe Demo App](https://github.com/carlodicelico/socialnetifyme)
  - [Slides for this talk](https://github.com/carlodicelico/rest-slides)


