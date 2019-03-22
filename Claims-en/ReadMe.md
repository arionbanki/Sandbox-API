# Claims API - Arion banki Fintech API documentation version v1
https://arionapi-sandbox.azure-api.net/claims/v1


### About Claims - Claims
This service contains information on claims that the logged in user has access to as the issuer of the claim. In the case of test users, random data is created when logging in for first time and continues to be used after that. The user also updates the data through their own actions and the data is retained between sessions.

The information is comparable to the data which users have access to via Arion Online Banking and Arion Bank’s B2B solutions, and there for not available working with identifiers, claimants and other operations at the moment.


### Security
Service requests need to contain an API key which approved teams in the hackathon will be able to get through the API portal.  Moreover the service is protected with OAuth 2.0 authentication, which includes either an authorization code or implicit flow.

At the moment the delimitation of authorizations is rather unsophisticated, an authenticated user gets access to all information under the resource.



---


## Claims



### /claims


* **get** *(secured)*: Returns a list of claims belonging to the claimant used to make the API request.
* **post** *(secured)*: Create a new claim.



### /claims/{claimId}


* **get** *(secured)*: Returns a representation of a claim.
* **patch** *(secured)*: Allows you to modify the properties of a claim. For example to cancel a claim.



### /claims/{claimId}/claimTransactions


* **get** *(secured)*: Returnes a list of transactions that encapsulate information about the status of a claim associated with a particular event in its lifetime.









