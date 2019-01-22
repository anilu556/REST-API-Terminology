# REST API Terminology

Fork and clone this repository. Then, push to github with all bad answers deleted and only the correct answers showing.

**1. What does it mean REST?**

Representational State Transfer.
A set of functions in which developers can perform requests and receive responses.

**2. Who coined the REST term?**

Dr. Roy Fielding.

**3. In which protocol REST is based?**

HTTP protocol such as GET and POST.

**4. What are the main building blocks of a REST Architecture?**
- Client and server. Architecture should have a client and server.
- Stateless client and server model. Server must not store any application data that is require to serve subsequent requests from client.
- Layered Client Cache Stateless Server Model. Could have multi level cache at client and server ends.
- Uniform Interface. Architecture should have these elements: Resource, Representations, Self Descriptive Messages, Hypermedia as the engine of application state.

Representations, Resources, Self Descriptive Messages, Hypermedia

**5. Identifying a resource is easy; you know how to access it and you even know how to request for a specific format. Since REST is using HTTP protocol as a standing point, there are some actions related to resources: CRUD operations.**

Complete the below table:+


|HTTP Verb|Proposed Action|
|---------|---------------|
|GET      |   Read        |
|POST     |   Create      |
|PUT      |   Update      |
|DELETE   |   Delete      |

**6. Status Code**

Another interesting standard that REST can benefit from when based on HTTP is the usage of HTTP status codes.

+ What’s is a status code?
 Standard response codes given by web site servers on the internet. The codes help identify the cause of the problem when a web page or other resource does not load properly.


+ Explain with your own words, the meaning of next codes:

|Status Code|Description                                                    |
|-----------|---------------------------------------------------------------|
|404        | Not found, the server could not find what was requested.      |
|200        | The request is ok.                                            |
|500        | The server has an internal error and can not make the request.|

**7. Status Code are grouped in five sets.**

Write what are their meaning.

|Group|Description  |
|-----|-------------|
|1XX  |Informational|
|2XX  |Success      |
|3XX  |Redirection  |
|4XX  |Client Error |
|5XX  |Server Error |

**8. HTTP Status Codes and Their Related Interpretation**

There are the most common status codes in HTTP responses. Please, fill with the required description.

|Status Code|Meaning              |
|-----------|---------------------|
|200        |Ok                   |
|201        |Created              |
|204        |No content           |
|301        |Moved permanently    |
|400        |Bad request          |
|401        |Unauthorized         |
|403        |Forbidden            |
|404        |Not found            |
|405        |Method not allowed   |
|500        |Internal Server Error|

###### [To see the full list of HTTP status codes and their meaning, please refer to the RFC of HTTP 1.1](http://tools.ietf.org/html/rfc7231#section-6)

**9. How are called the points of contact between all client apps and the API?**
Endpoints

**10. The following is a good example or bad example of a named access point? And why?**

_meant to list the books in a bookstore_

+ `GET /books/action1`

Is not describing what it is

**11. Uniform Interface**



To solve this problem, you can apply the REST style to the endpoints, and thanks to HTTP, you also have verbs to indicate actions.

|Old Style                 |REST Style              |
|--------------------------|------------------------|
|`/getAllBooks`            |  GET /books            |    
|`/submitNewBook`          |  POST /books           |
|`/updateAuthor`           |  PUT /authors/:id      |
|`/getBooksAuthors`        |  GET /books/:id/authors|
|`/getNumberOfBooksOnStock`|  GET /books/           |
|`/addNewImageToBook`      |  POST /books/:id/cover |
|`/getBooksImages`         |  GET /books/:id/cover  |
|`/addCoverImage`          |  POST /books/:id/cover |
|`/listBookCovers`         |  GET /books/:id        |

**12. What JSON does it mean?**

JavaScript Object Notation

**13. Anatomy of a `REQUEST`**

Make a `curl` request to _GitHub API_
Request information by an API
```sh
$ curl GET https://api.github.com/
```
According to the responded request, answer what does it mean the next parts from the handler:

+ _`Content-Type`_. Type of content u use
+ _`Status`_.  Code status
+ _`Date`_.
+ _`Content-Length`_. Length of the content.


###### If response is not showing those parts, ask to google how to print them in console.

```sh
# $ curl https://api.github.com/ --head
```
