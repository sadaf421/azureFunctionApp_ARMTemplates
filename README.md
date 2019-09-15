<h1> ARM Templates </h1>

This is a collection of JSON files that gives the ability to roll out Azure “Infrastructure as code" to be be used for the creation and deployment of Azure resources.
<br/>

<h1>Installation</h1>

To deploy these ARM templates, you will need to have Azure CLI installed. Please see links below;

<h3><B>Azure CLI</B></h3>

https://docs.microsoft.com/bs-latn-ba/cli/azure/install-azure-cli-windows?view=azure-cli-latest

<h1>Deployment</h1>


Now have installed  Azure CLI you are ready to deploy ARM templates. Please follow the below steps:
  * `az group deployment create  --name <deployment-name>   
   --resource-group <resource-group-name> 
   --template-file <file-name> 
   --parameters @<Param-file-name> 
   --out table`
   
     **Please note that you will need to fill the parameter values in parameters.json file to suit your needs.
   
   * If everything ran as expected you should be able to see deployment state as succeeded within the CLI itself. Once done, run the below command to fetch the git clone and web app url.
     <br/><br/>`az group deployment show -g <resource-group-name>   -n <deployment-name>   --query properties.outputs`
