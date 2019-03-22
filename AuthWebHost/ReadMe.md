# Management API - Arion banki Fintech API documentation version v1
https://arionapi-sandbox.azure-api.net/management/v1


### About Management - UserManagement
This service contains actions for working with clients and user registration for fintech sandbox.


### Security
Service requests need to contain an API key which approved teams in the hackathon will be able to get through the API portal. 
      



---


## Management
Used to register a Client, so the authorization server will recognize and correctly redirect tokens back to the solution.


### /clients


* **post**: Used to register a Client, so the authorization server will recognize and correctly redirect tokens back to the solution.





## User Management



### /users


* **post**: Makes it possible to get a new test user to use in the Fintech party sandbox. Note down the username and password, as it will not be shown again. The ClientID must be registered first.





## RB Json Web Token



### /rbjwt


* **get**: Returns the Jwt token to use with RBs API services.





