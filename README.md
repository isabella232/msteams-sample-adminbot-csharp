---
page_type: sample
products:
- office-365
languages:
- csharp
description: "TeamsAdminBot is a bot which allows admin to create teams, channels & add members dynamically."
urlFragment: teams-admin-bot
extensions:
  contentType: samples
  createdDate: "7/26/2018 9:06:01 AM"
---

# TeamsAdminBot

TeamsAdminBot is a bot which allows admin to create teams, channels & add members dynamically.

>**Note**: Currently, this code does not support adding Guest/Freemium users.

## Teams Admin Bot demo instance

There is a deployed demo instance of [TeamsAdminBot](https://teamsadminbot.azurewebsites.net) that anyone can talk to.

1. In order to try this bot please [sideload](https://docs.microsoft.com/microsoftteams/platform/concepts/apps/apps-upload#upload-your-package-into-a-team-using-the-store) the package present at `~\Manifest\TeamAdminBot.zip`.
2. Bot will send welcome message with options to create new teams or add members to existing.
3. You need to login before bot creates teams for you.
4. Once login is successful, click on create/modify teams button.
5. Bot will ask you to upload Teams details in an excel file. You can find sample input excel at `~\SampleInput.xlx`.
6. Just Upload the file attachment and wait for bot to create teams for you. 
>**Note**: [Send and receive files](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/bots/bots-files) feature require that you [enable Public Developer Preview mode](https://msdn.microsoft.com/en-us/microsoft-teams/publicpreview) in Microsoft Teams.


## How to deploy your own TeamsAdminBot

This guide is written for an [Azure](https://azure.microsoft.com) oriented as it uses [Azure Bot Service](https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-tutorial-authentication?view=azure-bot-service-3.0) for Authentication.

### Requirements
* [BotFramework Account](https://dev.botframework.com/)
* [Azure Account](https://azure.microsoft.com/en-us/)

### Steps
1. Create a Bot in [Azure](https://azure.microsoft.com/en-us/).
2. Register an [Azure AD v2 application](https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-tutorial-authentication?view=azure-bot-service-3.0#to-register-an-azure-ad-v2-application).
3. Replace appropriate values in `~\Web.config` i.e. MicrosoftAppId, MicrosoftAppPassword, ConnectionName & AzureWebJobsStorage with yours.
4. Run the Microsoft.Bot.Sample.TeamsAdmin project locally or deploy it on azure.
5. Update '~\Manifest\manifest.json` and replace "id" and "botId" with your app id.
6. Sideload this zip into any team of your choice using this [guide](https://msdn.microsoft.com/en-us/microsoft-teams/sideload).

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
