# Getting Started

1. First thing to do is to import all the environments into your Postman application. 
    The environments are a set of rules that tell postman what endpoint it should be contacting, for example production, Edog or Local deployment.
    To do this, go to the "Manage Environments" menu in the top right settings icon, open it and click on the import button.

    ![Manage_Environments-Import](/img/Manage_Environments-Import.gif)
Select all the files under the Environments folder and load them into Postman. Verify that all the new environments have been loaded by 
clicking in the drop down to the left of the "Manage Environments" menu.

    ![Manage_Environments-Import](/img/Manage_Environments-DropDown.gif)

2. Now that you have all the environments loaded into your workspace, is time to load a collection of requests. These are the actual HTTP requests that postman will use to contact the selected environment. To do this, go to "File > Import" and drag all the collections files under the Collections folder.

     ![Manage_Environments-Import](/img/Collection-Import.gif)

    This will load all the HTTP requests that have been preconfigured for use with the OneNote API.

3. Now that you have the collection loaded let's go ahead and add the Users and accounts that you will be using to send the requests.

    a) Go into the "Manage Environments" menu and click on the "Globals" button. Here you will see the settings postman will use to automatically generate AuthTokens.

    **DO NOT** add any sensitive information to the **Initial value** column of the variables, the initial value is exported and we don't want to share those values with others

    ![Manage_Environments-Import](/img/Manage_Environments-Globals.gif)

    b) Similarly you can edit any user specific ids (NotebookId, SectionId, tenantId etc...) by going to the collection variables tab and customizing the variables there. Right click over the Collection that you want to configure and select Edit. This will open the collection configuration, in here navigate to the variables tab and update any value you would want to use in your requests.

    ![Manage_Environments-Import](/img/Collection-Variables.gif)

    In the globals variables, you will need to fill the following values so that postman can get a valid AuthToken (Do this for each environment. e.g. GCC_UserName, GCCHigh_UserName, etc...):

    * *Prod*_UserName: The username for the account holding the notebooks you want to access using the onenote API (usually in the form of an email).

    * *Prod*_Password: The password to access the account specified in the username field.

    * client_id: The client id of the application that is requesting the account access. (This is shared across environments). Look at [this documentation](https://docs.microsoft.com/en-us/previous-versions/office/office-365-api/how-to/onenote-auth#register-your-application-and-get-a-client-id-and-secret-consumer-apps) to learn how to create a clientId.

    Once you have filled these fields save your changes and go back to the main postman screen.
    Now you should be able to open any of the requests and hit the Send button to execute it, postman will automatically fetch a new AuthToken whenever it is required.

## Local Environment Only - Configuring SSL

Your local deployment won't be reachable if you don't disable the use of "SSL certificate verification". To do this go to File > Settings > General and turn off the "SSL certificate verification".
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
