
### Prison Documentation 
[Prison Documents - Table of Contents](prison_docs_000_toc.md)

## Setting up PlaceholderAPI

This document provides a quick overview on how to install PlaceholderAPI.

Additional documentation on placeholders:

* [Guide: Prison Placeholders](prison_docs_310_guide_placeholders.md) 
	How to use placeholders. Includes HolographicDisplays.

* [Setting up Mines](prison_docs_101_setting_up_mines.md)
	This has a placeholder example using a One-block mine example with HolographicDisplays.


<hr style="height:1px; border:none; color:#aaf; background-color:#aaf;">



# Optional Dependencies

* If you want to use placeholders with plugins without placeholderAPI support you should also install the right version of [Protocollib](https://www.spigotmc.org/resources/protocollib.1997/) for you server and the [PlaceholderAPI ChatInjector](https://www.spigotmc.org/resources/chatinjector.38327/)


<hr style="height:1px; border:none; color:#aaf; background-color:#aaf;">



# Setting up PlaceholderAPI

Setting up PlaceholderAPI just need couple of steps:

* Download PlaceholderAPI
    - Go to the SpigotMC.org PlaceholderAPI download page
        - [PlaceholderAPI Download page](https://www.spigotmc.org/resources/placeholderapi.6245/)

* Copy to your server's plugin directory

* Restart your server. Do not use **/reload** or you'll break Prison Placeholders. Prison registers all of the placeholders upon server startup so the registrations will be lost.

<hr style="height:1px; border:none; color:#aaf; background-color:#aaf;">



# Placeholders Commands

Use the command **/prison placeholders** for a listing the placeholder commands.  These include:

* **/prison placeholders list**
* **/prison placeholders search <playerName> <pageNumber> <searchPatterns>**
* **/prison placeholders test <text>**

* **/prison version**

The listing of all the placeholders is available within the Prison startup information, and through `/prison version`.

<hr style="height:1px; border:none; color:#aaf; background-color:#aaf;">


# Troubleshooting Possible Compatibility Issues

There are no known issues with Prison and PlaceholderAPI, but out of the interest to help get your servers up and running, here are a couple of tips that could help with your environment.


<h3>Issue with PlaceholderAPI not working with Economy and Scoreboard</h3>

There was an issue with an economy placeholder not working with the QuickBoard placeholder.  

The solution was to download from PlaceholderAPI, their modified version of Vault and Essentials.  Followed by a server restart, or use `/papi reload`. 

```
/papi ecloud download Vault
/papi ecloud download Essentials
/papi reload
```

As a note, I'm not sure how well Prison behaves with the use of `/papi reload`.  It may be good to test with, but safer to just restart the server, once everything appears to be working and looks good.  The point is that any plugin reload is good to test with, but if you're going to let your server run for months, its probably best to do a clean restart.

With this example of installing the PlaceholderAPI and downloading their version of Vault and Essentials, the player reported that once the economy placeholder was working, another placeholder stopped working.  Their solution was to reinstall all of the papi (PlaceholderAPI) plugins (not sure if that includes reinstalling papi's version of Vault and Essentials) and then restarted the server.  The point here, is a clean start is probably helpful.


<hr style="height:1px; border:none; color:#aaf; background-color:#aaf;">
