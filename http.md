# HTTP

## REST (REpresentational State Transfer)? ##
### Methods ###

- Resource: URI
- Method: HTTP Method
- Representation or Message: JSON, XML etc.

CRUD (Create, Read, Update, Delete)


1.POST (Create)
-  Create new subordinate resources
-  ex) HTTP POST http://www.aaaaadomain.com/users
-  200 (OK) / 204 (No Content)

2.GET(Read)
- GET APIs should be idempotent
- ex) HTTP GET http://www.aaaaadomain.com/users?size=20&page=5

-  404 (Not Found) / 400 (Bad request)


3.PUT(Update)
- update existing resource
- 200 (OK) or 204 (No Content) / 404 (Not Found) 


4.DELETE(Delete)
-200 (OK). 404 (Not Found)



GET, PUT, DELET : idempotent

Uniform interface
Cacheable
Self-Descriptiveness

