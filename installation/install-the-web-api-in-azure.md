# Install the Web APIs in Azure

The FHIR Server consists of a number of decoupled ASP.NET Core Web APIs following a micro-services paradigm. In this example, we will install the 'Patient Service' API in an Azure Web App. The other APIs will follow the same process. The APIs can be found in the `medicloudconnect` GitHub account.

{% embed url="https://github.com/medicloudconnect" caption="" %}

## Create a Resource Group

In your Microsoft Azure account, create a `Resource group` for your FHIR Server APIs.

![](../.gitbook/assets/fhirrg.PNG)

## Create a Web App

In the Resource group, create a `Web App` for the API service

![](../.gitbook/assets/webapp_create.PNG)

## Create a Deployment

Open the Web App, and create a deployment in the `Deployment Center`, select the `External` repository option

![](../.gitbook/assets/deployment_centre1.PNG)

Use the `Kudu build server` for the deployment

![](../.gitbook/assets/kudu.PNG)

Enter the repository URL and branch for the deployment.

{% hint style="info" %}
Ensure that you enter the most recent 'release' branch and not 'master' to deploy a stable version of the application. You can find the repository URLs for the APIs in the `medicloudconnect` GitHub account.
{% endhint %}

{% embed url="https://github.com/medicloudconnect" caption="" %}

![](../.gitbook/assets/public_gitrepo.PNG)

Wait for the repository to build and the deployment to complete. A successful deploy will be indicated in the portal.

![](../.gitbook/assets/deploy_success.PNG)

You can now preview the Web App in the browser by clicking the `URL` link.

![](../.gitbook/assets/web_app_preview.PNG)

![](../.gitbook/assets/web_app_preview2.PNG)

