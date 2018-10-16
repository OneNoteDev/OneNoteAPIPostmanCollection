# Getting Started

1.- First thing to do is to import all the environments into your Postman application. 
    The environments are a set of rules that tell postman what endpoint it should be contacting, for example production, Edog or Local deployment.
    To do this, go to the "Manage Environments" menu in the top right settings icon, open it and click on the import button. 
    Select all the files under the Environments folder and load them into Postman. Verify that all the new environments have been loaded by 
    clicking in the drop down to the left of the "Manage Environments" menu.

2.- Now that you have all the environments loaded into your workspace, is time to load a collection of requests. These are the actual HTTP requests
    that postman will use to contact the selected environment. To do this, go to "File > Import" and drag all the collections files under the Collections folder.
    This will load all the HTTP requests that have been preconfigured for use with the OneNote API.

3.- The last thing to do is to specialize your collection to your local environment, this will tell postman what parameters to use for your machine and for your specific request scenarios.
    a.- Right click over the Collection that you want to configure and select Edit. This will open the collection configuration, in here navigate to the variables tab. 
        Look for the "MachineName" parameter and add your machine's name TO THE "CURRENT VALUE" ONLY 
            *** Do not add any of these local parameters to the initial value, the initial value is exported and we don't want to share these parameters with others *** 
    b.- Go back into the "Manage Environments" menu and click on the "Globals" button. Here you will see the two different types of AuthTokens used to contact Production or PPE environments. 
        Add the necessary auth tokens to these variables (CURRENT VALUE ONLY) and hit save. The AuthTokens will expire after a while so you will have to come back and update their values every time
        that happens.

Now you should be able to open any of the requests and hit the Send button to execute.

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
