
#  🚪 What are Backdoors and how to prevent them
  
Preventing backdoors on your server is **__CRUCIAL__** to maintaining server security, if an unauthorized third party gains access to your server, your files, players and even yourself may be at risk depending on the severity,  
  ``NOTE TO LUNA: everything with __'s before and after is intenteded to be underlined but for some reason stackedit isn't underlining them.``
  > Author, @zoamm
## 🔐  Preventing Backdoors  
  
This is __**not**__ a full-proof guide to prevent backdoors on your server(s). This article simply serves as a guide to prevent you from making bad decisions, as-well as enabling some key features.
###  1. What's a backdoor?
  In short, a backdoor is a malicious file or code that someone adds to your server, this malicious code is often hidden in addons, scripts or even models. This malicious code allows the person who installed them to run unauthorized commands such as giving themselves and others superadmin, changing the map, downloading your server files, and much more.
### 2. Your Server Addons  
People with malicious intent may try to incentive you as a community owner into adding their addon to your server, only you or a trusted individual (such as a trusted developer), should have access to adding addons to your server, this includes workshop addons. We recommend __never__ adding non-verified addons into your server. You can get safe ready-to-use addons at [gmodstore](https://www.gmodstore.com/), these addons have been verified by the gmodstore team and do not contain any malicious code.
[![image](https://i.imgur.com/VQVBHWb.png)](https://www.gmodstore.com/)
### 3. Avoiding leaked addons  
Leaked addons are notorious for having backdoors inside them, using an addon that has been leaked onto a forum or given to you by someone is an easy way to get backdoored and possibly have your server shutdown. Using leaked addons is prohibited by Physgun and avoiding them entirely will help keep your server safe.

### 4. Custom Content
If your server provides a service where you add a workshop model/item onto your server for a player, you should be **EXTREMELY** cautious before adding these addons to your server, we recommend get a qualified/trusted developer to inspect the addon before you proceed (if you know what your doing you can inspect the addon yourself). Secondly, you should extract the addon using a software like [gmpublisher](https://github.com/WilliamVenner/gmpublisher), and add it directly to your `/addons` folder instead of updating your workshop.
![image2](https://imgur.com/7IAQKzK.png)

### 5. Disable workshop autoupdate  
This is an extremely important step! One of the most popular ways that a server gets backdoored is via a workshop update. After someone has gotten their workshop addon into your server, they will update their addon, this time adding malicious code inside, If your server doesn't disable automatic updates, your server can be at great risk. To disable this simply log into your server and type `host_workshop_autoupdate 0`
![image1](https://i.imgur.com/MHJkOmd.png)
If later on you want to update an addon, first verify it contains no malicious code and then simply remove and re-add the addon to your content pack, this will manually update the addon to your server. 
|| **Remember:** It is your responibility to protect the integrity and security of your server and your players, there is not a push-a-button method that will prevent your server from ever getting backdoored, be cautious of adding addons to your server and only give panel access to those whom you trust.