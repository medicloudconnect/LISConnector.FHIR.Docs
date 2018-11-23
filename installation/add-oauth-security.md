# Add OAuth Security

The Web APIs are protected with the **OAuth 2 Client Credentials** flow. We will use **Azure Active Directory \(AAD\)** for security.

## Create a FHIR Server App Registration

Open Azure Active Directory \(AAD\) and create an new `App registration` for the FHIR Server.

![](../.gitbook/assets/aad_fhirserver.PNG)

## Create a FHIR Client App Registration

Create another `App registration` for the FHIR Client.

![](../.gitbook/assets/aad_fhirclient.PNG)

## Add a Required Permission for the FHIR Client to access the FHIR Server

Open the **FHIR Client** application, and add a `Required permission` by clicking the `+Add` icon.

![](../.gitbook/assets/aad_req_permissions.PNG)

Select the FHIR Server for access

![](../.gitbook/assets/aad_selectapi.PNG)

Then select the `Delegated Permission` as shown below. Click the 'done' icon when you are completed.

![](../.gitbook/assets/aad_selectpermission.PNG)

## Add a Client Secret

In the Settings section of the **FHIR Client**, click on keys and add a `ClientSecret` key. Copy the key and paste it in a secured location to use later.

![](../.gitbook/assets/aad_clientsecret.PNG)

## Protect the web API with OAuth

Open the Web App, click on the `Application settings` and add the following settings:

![](../.gitbook/assets/aad_config%20%281%29.PNG)

`AzureAd:ClientId` - The `Application ID` of the **FHIR Server** application.

![](../.gitbook/assets/aad_clientid.PNG)

  
`AzureAd:Domain` - The domain of your Azure Active Directory account.

![](../.gitbook/assets/aad_domain.PNG)

`AzureAd:Instance` - The url for the Azure Active Directory security endpoints. This value should be : `https://login.microsoftonline.com/`

`AzureAd:TenantId` - The `Directory ID` of your Azure Active Directory

![](../.gitbook/assets/aad_tenantid.PNG)

