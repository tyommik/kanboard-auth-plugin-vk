VK [Vkontakte] Authentication
=====================

VK OAuth2 authentication plugin based on generic plugin.

Author
------

- Artem Shibaev
- License MIT

Requirements
------------

- Kanboard >= 1.0.37

Installation
------------

You have the choice between 3 methods:

1. Install the plugin from the Kanboard plugin manager in one click
2. Download the zip file and decompress everything under the directory `plugins/OAuth2`
3. Clone this repository into the folder `plugins/OAuth2`

Note: Plugin folder is case-sensitive.

Configuration
-------------

Go to the application settings > integrations > OAuth2 Authentication.

### 1) Create a new application on the VK provider

Go to the third-party authentication provider and add a new application. 
Copy and paste the **Kanboard callback URL** and generate a new set of tokens.

The third-party provider will returns a **Client ID** and a **Client Secret**.
Copy those values in the Kanboard's settings.

### 2) Configure the provider in Kanboard

- **Client ID**: Unique ID that comes from the third-party provider
- **Client Secret**: Unique token that comes from the third-party provider
- **Authorize URL**: URL used for authorization
- **Token URL**: URL used to get tokens from third-party provider
- **User API URL**: URL used to fetch user profile after authentication
- **Username Key**: Key used to fetch the username from the user API response
- **Name Key**: Key used to fetch the full name
- **Email Key**: Key used to fetch the user email
- **User ID Key**: Key used to fetch the unique user ID

Examples
--------

Example for VK:

- **Authorize URL**: `https://oauth.vk.com/authorize`
- **Token URL**: `https://oauth.vk.com/access_token`
- **User API URL**: `https://api.vk.com/method/users.get?fields=screen_name,id,email&v=5.92`
- **Scopes**: `notify`
- **Username Key**: `screen_name`
- **Name Key**: `first_name,second_name` (This doesn't matter now, is used first_name + last_name)`
- **Email Key**: `email`
- **User ID Key**: `id`
