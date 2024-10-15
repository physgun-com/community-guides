# 💰 Connect your Donation System to your Garry's Mod Server

Author: Penguin, Admin of Arctic Networks

This guide will cover how to set up the Noclip, Ember & Prometheus donation systems for your Garry's Mod server.

## Requirements

You will need one of the following donation systems before continuing.

* [Noclip (Free)](https://noclip.gg)
* [Ember (Paid)](https://www.gmodstore.com/market/view/ember-donation-system-bans-loading-screen-landing-index-page)
* [Prometheus (Paid)](https://www.gmodstore.com/market/view/prometheus)

**Note |** Noclip is significantly easier to set up if you are new to owning Garry's Mod servers. Ember & Prometheus are also self-hosted, meaning you will need to set up Web Hosting of your own.

## Noclip (Easy)

Noclip is by far the easiest system to set up, as the Garry's Mod Lua comes pre-configured to sync with your website.

### Step Process

1. Login to your Noclip account and set up a community if you haven't already.
2. Go to `Dashboard -> Servers (Under "Store") -> New Server`
3. Fill out all the required information (Marked with *), You can get your Server IP & Port from the Game Panel. You may need to separate **IP:PORT**.
4. Select **"Create"** and you should be re-directed back to the **Servers Tab**.
5. Select **"Download Addon"** next to the server you have just added.
6. Install the addon under ``garrysmod->addons`` in your server.
7. **Additionally:** Install ``reqwest`` under ``Tools -> Mod Manager`` so that the server can communicate with the website.
8. Restart your server and check for errors in the console.

If there are no errors, great! It is still worth testing to see if packages are given to players. Additionally, you can test the store yourself with a 100% coupon.

If you do experience any errors, you can get Noclip support under the [Physgun Official Discord](https://physgun.com/discord)

Find the full Noclip documentation [here!](https://ember-docs.kekalainen.me/installation/web.html)

## Ember (Medium)

Ember is a self-hosted platform that also supports a Donation Store, If you have not linked the Garry's Mod community to your website yet (therefore not being able to collect donations), this tutorial should be able to help!

### Step Process

1. Go to ```Admin -> Servers``` and select the + icon to add a new server.
2. Fill out the ``Server Name``, ``Server IP``, ``Game Port`` (Query port can be the same) and select ``Garrys Mod`` for the type of server. You can get your Server IP & Port from the Game Panel. You may need to separate **IP:PORT**.
3. Select the refresh symbol under ``Token`` to generate a new token and copy it to the clipboard.
4. Install the Garry's Mod Ember addon, which is provided under ``lua/ember`` when downloading from GModStore.
5. Restart your server, then run the following command in console: ``ember connect (Website URL) (Token)`` with website url being the domain of your website and token being what you copied earlier.

Find the full Ember documentation [here!](https://ember-docs.kekalainen.me/configuration/server.html)

## Prometheus (Hard)

Prometheus notoriously causes a lot of difficulty when setting up, especially for those not as experienced in operating web servers. Follow this guide closely, and you should be able to successfully connect the web & gmod together.

### Pre-setup (If you haven't already setup a database)

1. Login to CPanel. (Can be accessed through most client areas.)
2. Locate ``Manage My Databases`` under ``Databases``.
3. Create a new database, and give it a rememberable name.
4. Create a user with a username and password (also rememberable but secure).
5. Add the user (you just created) to the database (you just created) and give it all privileges.
6. Use this information and apply it where necessary when setting up prometheus on the web. (You will also need it for setting up Garry's Mod.)

**Another Important Step:**

1. Locate ``Remote Database Access`` under ``Databases`` on CPanel.
2. Allow connection from either your GMod Server's IP Address or % (Allow connections from anywhere)
3. This is **required** allow connections to be made between the Garry's Mod Server & The Website.

### Step Process
1. Go to ``Admin -> Servers -> Add``, and select Garry's Mod as the game and fill out the server name.
2. Click ``Submit`` and collect the Server ID (You will need this later).
3. Install ``MySQLOO`` under ``Tools -> Mod Manager`` so that the server can connect with the remote database.
4. Install the Garry's Mod Prometheus addon, which is provided under ``lua/addons/prometheus`` when downloading from GModStore.
5. Find the configuration file under ``prometheus/lua/prometheus_config.lua`` and set the ``Server ID`` to the Server ID on the website.
6. Go to CPanel, and from the dashboard copy to clipboard your ``Shared IP Address``. You will use this as the ``Host`` when setting up the GMod addon.
7. Fill out the ``Host``, ``Username``, ``Password`` & ``Database Name`` with the exact same information that was used when setting up the website.
8. Restart the server.
9. Go back to the website, Go to ``Admin -> Dashboard -> Other features`` and send a test message to see if the connection is successful.
10. Check for any errors in console, they are quite descriptive so its likely you will be able to find the problem and resolve it.

Find the full Prometheus documentation [here!](https://wiki.prometheusipn.com/index.php?title=Main_Page#Installation)
