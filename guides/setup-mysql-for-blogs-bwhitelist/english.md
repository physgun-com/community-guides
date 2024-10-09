# 💽 How to setup MySQL for bLogs and bWhitelist (GModAdminSuite)

In this guide we'll go over setting up a MySQL database to your GModAdminSuite addons, whether it be bLogs, bWhitelist this guide applies to both!

## Requirements
Before connecting your database you'll need to setup a couple of things. Such as an existing database and the `gas-config` addon.

* [Installing GmodAdminSuite (GAS Config)](https://help.physgun.com/en/article/how-to-install-gmodadminsuite-f0znnj/)
* [Creating a MySQL database](https://help.physgun.com/en/article/how-to-create-a-mysql-database-194xolo/)
* [Installing MySQLOO](https://help.physgun.com/en/article/how-to-install-mysqloo-for-your-garrys-mod-server-drvt9q/)

### Connecting the database to GModAdminSuite
GModAdminSuite basically connects various server management addons such as bLogs, bWhitelist, bAdminSits, etc.. So we'll only need to fill in the `gas-config` for MySQL details!

1. Navigate to Your Server in the [Physgun Gamepanel](https://gamecp.physgun.com)
2. Navigate to `Management` > `File Manager`
3. Navigate to `/garrysmod/addons/gas-config/lua/gmodadminsuite_mysql_config.lua` in the File Manager
![Navigating to the MySQL config](https://storage.crisp.chat/users/helpdesk/website/b7104a41488ce800/firefoxzrapzozfv6_d9w1qf.gif)
4. Fill in the `Host`, `Username`, `Database Name`, and `Password`.
5. Ensure you have set `GAS.Config.MySQL.Enabled` to `true`
6. Click `Save File` on the bottom right
7. Restart your server and you're done!
