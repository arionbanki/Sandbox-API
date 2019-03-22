# Accounts API - Arion banki Fintech API documentation version v1
https://arionapi-sandbox.azure-api.net/accounts/v1


### About Accounts - Deposit accounts
This service contains information on bank accounts to which a logged in user has access. In the case of test users, random data is created when logging in for first time and continues to be used after that.

The information is comparable to the data which users have access to via Arion Online Banking, Arion App and Arion Bank’s B2B solutions. The user can both view their current and savings accounts.  The basic information for each account is displayed and transactions and balances can be viewed for each account.
      


### Security
Service requests need to contain an API key which approved teams in the hackathon will be able to get through the API portal.  Moreover the service is protected with OAuth 2.0 authentication, which includes either an authorization code or implicit flow.

At the moment the delimitation of authorizations is rather unsophisticated, an authenticated user gets access to all information under the resource.



---


## Accounts



### /accounts


* **get** *(secured)*: Retrieves information about available accounts.



### /accounts/{accountId}
A single account identified by account ID.

* **get** *(secured)*: Information about an account.



### /accounts/{accountId}/accountTransactions
Provides an overview of account transactions. It is not permitted to get all transactions at once. Instead you have to define page number and transactions per page.

* **get** *(secured)*: Returns list of transactions that can be filtered by transaction date. It is possible to get the data by defining page number and page size.









