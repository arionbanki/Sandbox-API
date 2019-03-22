# Digital Signature API - Arion banki Fintech API documentation version v1
https://arionapi-sandbox.azure-api.net/digitalSignatures/v1


### About DigitalSignature - DigitalSignatures
This services shows the options for signing documents. In the test environment it is always Arion Bank which requests that a document be signed, and real ID numbers need to be provided for the people signing. Documents are signed  using [https://prufa.signet.is/](https://prufa.signet.is/ "Signet prófunarumhverfi")

Similar to the options offered by Signet although the API interfaces makes certain things in this first phase easier.


### Security
Service requests need to contain an API key which approved teams in the hackathon will be able to get through the API portal.  Moreover the service is protected with OAuth 2.0 authentication, which includes either an authorization code or implicit flow.

At the moment the delimitation of authorizations is rather unsophisticated, an authenticated user gets access to all information under the resource.



---


## Digital signatures



### /digitalSignatures


* **post** *(secured)*: Creates a new digital signature



### /digitalSignatures/{uuid}
Universal unique identifier for signature.

* **get** *(secured)*: 
* **delete** *(secured)*: 



### /digitalSignatures/{uuid}/documentContent
The document that is to be signed by the receiving parties

* **get** *(secured)*: Gets the content.
* **post** *(secured)*: Uploads the file content to be digitally signed. Until this has happened, the signature remains invalid.
After the upload is finished, the processing starts.










