# Management API - Arion banki Fintech API documentation version v1
https://arionapi-sandbox.azure-api.net/management/v1


### Um Management - Notendastjórnun
Undir þessari þjónustu er að finna aðgerðir til að vinna með biðlara og notendaskráningu, fyrir Fintech sandkassann.


### Öryggi
Köll á þjónustuna þurfa að innihalda API lykil sem samþykkt teymi í Fintech Party munu geta sótt um á gátt API viðmótsins. 
      



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





