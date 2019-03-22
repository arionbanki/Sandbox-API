# National Registry API - Arion banki Fintech API documentation version v1
https://arionapi-sandbox.azure-api.net/nationalregistry/v1


### About NationalRegistry - NationalRegistry
This service allows the logged in user to perform a search in the National Registry, if permitted to do so. Similar to searches the user can perform in Online Banking. A certain cohort of ID numbers is used for access to test data.


### Security
Service requests need to contain an API key which approved teams in the hackathon will be able to get through the API portal.  Moreover the service is protected with OAuth 2.0 authentication, which includes either an authorization code or implicit flow.

At the moment the delimitation of authorizations is rather unsophisticated, an authenticated user gets access to all information under the resource.



---


## National Registry Parties



### /nationalRegistryParties


* **get** *(secured)*: Returns information about parties from the Icelandic National Registry, both individuals and corporations.



### /nationalRegistryParties/{kennitala}
A valid kennitala.

* **get** *(secured)*: A uniquely identifiable party, by kennitala.







