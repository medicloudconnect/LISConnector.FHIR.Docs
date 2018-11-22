# Testing the API with Postman

You can test the APIs with the Postman application. You can download and install Postman from their site.

{% embed url="https://www.getpostman.com/apps" %}

  
Before completing this section , you should have completed the previous section of this guide:

{% page-ref page="add-oauth-security.md" %}

###  Get a JWT Token

You will need to get a JWT token to access the OAuth secured API. The token URL is in the format `https://login.microsoftonline.com/<TenantId>/oauth2/token`

The `TenantId` is the Directory ID of your Azure Active Directory \(AAD\) that was used to secure the API.

![](../.gitbook/assets/aad_tenantid.PNG)

Set the following authorization parameters in the body of your `POST` request

![](../.gitbook/assets/pm_authbody.PNG)

  
`grant_type` : The is th OAuth grant type, it should be set to `client_credentials`

`client_id` : This is the Application Id of the FHIR Client application that was created in AAD

![](../.gitbook/assets/pm_clientid.PNG)

`client_secret` : This is the Client Secret of the FHIR Client

![](../.gitbook/assets/aad_clientsecret.PNG)

`resource` - This is the Application Id of the FHIR Server that we are trying to access from the client

![](../.gitbook/assets/aad_clientid.PNG)

  
When you send the POST request with Postman , you should get the Access Token in the response.

![](../.gitbook/assets/pm_access_token.PNG)

