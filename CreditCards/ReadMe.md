# Creditcards API - Arion banki Fintech API documentation version v1
https://arionapi-sandbox.azure-api.net/creditcards/v1


### CreditCards - CreditCards
This service contains information on credit cards to which a logged in user has access. In the case of test users, random data is created when logging in for first time and continues to be used after that.

The information is comparable to the data which users have access to via Arion Online Banking, Arion App and Arion Bank’s B2B solutions. You can find information on the different features of each card and view transactions for each period.


### Security
Service requests need to contain an API key which approved teams in the hackathon will be able to get through the API portal.  Moreover the service is protected with OAuth 2.0 authentication, which includes either an authorization code or implicit flow.

At the moment the delimitation of authorizations is rather unsophisticated, an authenticated user gets access to all information under the resource.



---


## CreditCards
Provides an overview of credit cards


### /creditCards


* **get** *(secured)*: Provides an overview of credit cards. It provides information on cards where the logged-in user is a cardholder or owner of a card, provided that user is entitled to see the credit card. It shows information on cards in active use and cards in the legal collection process. It does not show amounts on cards in the legal collection process as collection costs are not included in the balance. In such cases null is returned in the field for amounts



### /creditCards/{cardId}
Provides detailed information on individual cards.

* **get** *(secured)*: Provides detailed information on individual cards. The logged in user has to be a cardholder or the owner of a card and also have permission to see the card. It does not show amounts on cards in the legal collection process as collection costs are not included in the balance. In such cases null is returned in the field for amounts.



### /creditCards/{cardId}/creditCardTransactions
Provides an overview of credit card transactions.It is not permitted to get all transactions at once. Instead you have to define page number and transactions per page.

* **get** *(secured)*: Allows the user to view the transactions on a card performed during a specific period. The logged-in user has to be a cardholder or the owner of a card and also have permission to see the card. It is possible to get the data by defining page number and page size.









