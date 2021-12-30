## Week 14 Homework: Web Development


#### HTTP Requests and Responses

Answer the following questions about the HTTP request and response process.

1. What type of architecture does the HTTP request and response process occur in? Client-Server model.

2. What are the different parts of an HTTP request? 
The HTTP request is a series of requests and responses.

3. Which part of an HTTP request is optional? The request body.

4. What are the three parts of an HTTP response?
 The request line, the header, and the whitespace are the three components in the response.

5. Which number class of status codes represents errors? 400-499.

6. What are the two most common request methods that a security professional will encounter?
GET and PUT.

7. Which type of HTTP request method is used for sending data? The POST method

8. Which part of an HTTP request contains the data being sent to the server? POST method

9. In which part of an HTTP response does the browser receive the web code to generate and style a web page? The PUT method.

#### Using curl

Answer the following questions about `curl`:

10. What are the advantages of using `curl` over the browser? It allows for adjustments as you work from the command line whereas the browser doesn't do that.

11. Which `curl` option is used to change the request method?
-X followed by the type of method to use.

12. Which `curl` option is used to set request headers?
 The --headers flag will set request headers.

13. Which `curl` option is used to view the response header? 
The --head flag will only show the response header.

14. Which request method might an attacker use to figure out which HTTP requests an HTTP server will accept? The POST method to see if the server will allow data to be added.

#### Sessions and Cookies

Recall that HTTP servers need to be able to recognize clients from one another. They do this through sessions and cookies.

Answer the following questions about sessions and cookies:

15. Which response header sends a cookie to the client? Set-Cookie: cart=Bob.

    ```HTTP
    HTTP/1.1 200 OK
    Content-type: text/html
    Set-Cookie: cart=Bob
    ```

16. Which request header will continue the client's session? GET /cart HTTP/1.1

    ```HTTP
    GET /cart HTTP/1.1
    Host: www.example.org
    Cookie: cart=Bob
    ```

#### Example HTTP Requests and Responses

Look through the following example HTTP request and response and answer the following questions:

**HTTP Request**

```HTTP
POST /login.php HTTP/1.1
Host: example.com
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Type: application/x-www-form-urlencoded
Content-Length: 34
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Mobile Safari/537.36

username=Barbara&password=password
```

17. What is the request method? POST

18. Which header expresses the client's preference for an encrypted response? Upgrade-Insecure-Requests: 1

19. Does the request have a user session associated with it? No

20. What kind of data is being sent from this request body? A log in form.

**HTTP Response**

```HTTP
HTTP/1.1 200 OK
Date: Mon, 16 Mar 2020 17:05:43 GMT
Last-Modified: Sat, 01 Feb 2020 00:00:00 GMT
Content-Encoding: gzip
Expires: Fri, 01 May 2020 00:00:00 GMT
Server: Apache
Set-Cookie: SessionID=5
Content-Type: text/html; charset=UTF-8
Strict-Transport-Security: max-age=31536000; includeSubDomains
X-Content-Type: NoSniff
X-Frame-Options: DENY
X-XSS-Protection: 1; mode=block

[page content]
```

21. What is the response status code? 200

22. What web server is handling this HTTP response? Apache

23. Does this response have a user session associated to it? Yes, SessionID=5

24. What kind of content is likely to be in the [page content] response body? Text file.

25. If your class covered security headers, what security request headers have been included?
Transport security, No packet sniffing, Block cross site
#### Monoliths and Microservices

Answer the following questions about monoliths and microservices:

26. What are the individual components of microservices called? A web Stack

27. What is a service that writes to a database and communicates to other services? The backend server ex: PHP, Perl, Python

28. What type of underlying technology allows for microservices to become scalable and have redundancy? Container services such as docker.

#### Deploying and Testing a Container Set

Answer the following questions about multi-container deployment:

29. What tool can be used to deploy multiple containers at once? Docker compose

30. What kind of file format is required for us to deploy a container set? A YAML file is used to deploy a container set

#### Databases

31. Which type of SQL query would we use to see all of the information within a table called `customers`? While in an SQL session run SELECT * FROM customers;

32. Which type of SQL query would we use to enter new data into a table? (You don't need a full query, just the first part of the statement.) Run the query INSERT INTO table_name 

33. Why would we never run `DELETE FROM <table-name>;` by itself? It will delete all the information associated within that table!

---

