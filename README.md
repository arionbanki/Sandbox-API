# Documentation for Arion's API offering in hackathons

# API definitions
https://github.com/arionbanki/Sandbox-API
* [Accounts - innlánsreikningar](https://github.com/arionbanki/Sandbox-API/tree/master/Accounts)  
* [CreditCards - greiðslukort](https://github.com/arionbanki/Sandbox-API/tree/master/CreditCards)  
* [Claims - innheimtukröfur](https://github.com/arionbanki/Sandbox-API/tree/master/Claims)
* [NationalRegistry - þjóðskrá](https://github.com/arionbanki/Sandbox-API/tree/master/NationalRegistry)
* [Currency - gengisupplýsingar](https://github.com/arionbanki/Sandbox-API/tree/master/Currency)


# 1. Getting API Credentials

To use the API you need a developer key.
Portal for creating an developer key, as described below. 
https://arionapi-sandbox.portal.azure-api.net

* [Sign into the API portal](https://arionapi-sandbox.portal.azure-api.net/signin?ReturnUrl=%2Fproducts)

* [Arion Sandbox](https://arionapi-sandbox.portal.azure-api.net/products/arion-fintech-api)
Select **Add subscription**, and type Subscription name of your own chose in subscription name

Select **Confirm**

You can then find your subscription here:
[Arion Sandbox](https://arionapi-sandbox.portal.azure-api.net/products/arion-fintech-api)

You have 1 subscription to this product:

There will be link below to your subscription/developer page

Select your **Subscription**

In the [Developer profile page](https://arionapi-sandbox.portal.azure-api.net/developer)

You are provided with two developer keys for every subscription: Primary and Secondary


# 2. Getting Client ID and Client Secret
 
To register your client in IdentityServer, you need to provide 3 things:

**ClientId** - client id of your own choice etc. AppTeam1

**RedirectUrl** - when authenication is done in the app, our identityserver will redirect to your url

**OAuth Grant type** - Implicit/Code.

Implicit flow is usually targeted at SPA Apps (and any other Javascript/User-agent-based app)

Code flow is usually targeted at web applications or other systems that have a server-side component that can act as a Confidential Client (keep the client secret secure)

| OAuth Grant type | Client Registration Url |
| ---------------- |:-------------:|
| Implicit flow    | https://arionapi-identityserver3-sandbox.azurewebsites.net/clientregistration?clientId=YOURCLIENTID&redirectpath=http://yourhost/yourpath/yourcallback&flowType=implicit |
| Code flow | https://arionapi-identityserver3-sandbox.azurewebsites.net/clientregistration?clientId=YOURCLIENTID&redirectpath=http://yourhost/yourpath&flowType=code |

You will be prompted with: YOURCLIENTID registered, your secret is: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx - please store it carefully, you will never see this again!

# 3. Assign Registered client to a user
Select **Browser** of your choice and goto the url below.
Use the clientId you chose in Step 2.
https://arionapi-identityserver3-sandbox.azurewebsites.net/NewUser?clientId=YOURCLIENTID |

You will be prompted with: Username: John Doe, Password: xxxxxxxxx - please store it carefully, you will never see this again!

# Scopes
| Sope       | Description   |
| ---------- |:-------------:|
| financial  | Access to all financial operations. |

# OAuth endpoints
| Endpoint | Url   |
| --------- |:-------------:|
| Authorize | https://arionapi-identityserver3-sandbox.azurewebsites.net/connect/authorize |
| Token     | https://arionapi-identityserver3-sandbox.azurewebsites.net/connect/token |


# Examples

## Web example Implicit client ( etc. Javascript or Python ) use the url to get otken:
----------------------------------------------------------------------------
https://arionapi-identityserver3-sandbox.azurewebsites.net/connect/authorize?response_type=token&client_id=YOURCLIENTID&redirect_uri=https%3a%2f%2fyourhost%2fyourpath%2f%2fyourcallback&scope=financial


## Example of getting token using our FintechAzureApiManagement client. (We would recommend you to use your own client_id. Provided in the Arion API portal)
https://arionapi-identityserver3-sandbox.azurewebsites.net/connect/authorize?response_type=token&client_id=FintechAzureApiManagement&redirect_uri=https%3a%2f%2farionapi-sandbox.portal.azure-api.net%2fdocs%2fservices%2f57361a83110546175c6fec3d%2fconsole%2foauth2%2fimplicit%2fcallback&state=aae016ca-1c17-42bc-99d2-122c8470b0d9&scope=financial

[node.js Demo of getting token](https://github.com/arionbanki/nodejs-Sandbox-API-Demo/)


# Tools
[Url-encoder for redirect urls](http://meyerweb.com/eric/tools/dencoder)

[JWT.IO allows you to decode, verify and generate JWT.](https://jwt.io)
