# Getting Started

1.- First thing to do is to import all the environments into your Postman application. 
    The environments are a set of rules that tell postman what endpoint it should be contacting, for example production, Edog or Local deployment.
    To do this, go to the "Manage Environments" menu in the top right settings icon, open it and click on the import button. 

![Manage_Environments-Import](/img/Manage_Environments-Import.gif)

    Select all the files under the Environments folder and load them into Postman. Verify that all the new environments have been loaded by 
    clicking in the drop down to the left of the "Manage Environments" menu.

![Manage_Environments-Import](/img/Manage_Environments-DropDown.gif)

2.- Now that you have all the environments loaded into your workspace, is time to load a collection of requests. These are the actual HTTP requests
    that postman will use to contact the selected environment. To do this, go to "File > Import" and drag all the collections files under the Collections folder.

![Manage_Environments-Import](/img/Collection-Import.gif)

    This will load all the HTTP requests that have been preconfigured for use with the OneNote API.

3.- The last thing to do is to specialize your collection to your local environment, this will tell postman what parameters to use for your machine and for your specific request scenarios.
    a.- Right click over the Collection that you want to configure and select Edit. This will open the collection configuration, in here navigate to the variables tab. 
        Look for the "MachineName" parameter and add your machine's name TO THE "CURRENT VALUE" ONLY 
            *** Do not add any of these local parameters to the initial value, the initial value is exported and we don't want to share these parameters with others *** 

![Manage_Environments-Import](/img/Collection-Variables.gif)

    b.- Go back into the "Manage Environments" menu and click on the "Globals" button. Here you will see the two different types of AuthTokens used to contact Production or PPE environments.
![Manage_Environments-Import](/img/Manage_Environments-Globals.gif)

You can use the ticketizer tool to create the AuthTokens: http://toolbox/ticketizer
Open the tool, go to the ADAL tab and hit the "Ticket Please!!" button to the right:
![Manage_Environments-Import](/img/CreateAuthToken.gif)

This will generate a token for the production environment token. Copy the token from there and paste it in the "Prod_AuthToken" variable current value.
You can also generate a token for the "PPE_AuthToken" variable by clicking in the "INT/PPE" radio button in ticketizer before generating the token.
![Manage_Environments-Import](/img/CreateAuthToken_PPE.gif)

Add the necessary auth tokens to these variables (CURRENT VALUE ONLY) and hit save. 

The AuthTokens will expire after a while so you will have to come back and update their values every time
that happens.

Now you should be able to open any of the requests and hit the Send button to execute.

# Configuring SSL

Your local devfabric deployment won't be reachable if we don't disable the use of "SSL certificate verification". To do this go to File > Settings > General and turn off the "SSL certificate verification".
![Manage_Environments-Import](/img/DisableSSL.gif)

# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
