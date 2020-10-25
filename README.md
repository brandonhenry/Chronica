# *Chronica Project*

### Drupal Setup & Installation

*Following this guide for setting up Drupal:* [https://www.drupal.org/docs/installing-drupal*](https://www.drupal.org/docs/installing-drupal) 



#### Local Server Setup

In order to install and run Drupal, a server and PHP are needed to host the contents. In order to have a publicly accessible server, web hosting and a domain are needed. 



For simplification, we decided to use the Acquia AMP stack to test and develop the Drupal site locally. More information about Acquia can be found here: https://dev.acquia.com/downloads.



![Acquia Info](C:\Users\itsbh\Documents\GitHub\Chronica\Doc\Images\Acquia Info.png)



When installing, the default port settings were used:

**Web Server HTTP port: 8083**

**Web Server HTTPS port: 8443**

**MySQL Database Port: 33067**



#### Repository

To allow easy access to files, the Chronica project can be accessed and deployed via the GitHub link here: https://github.com/brandonhenry/Chronica



#### Drupal Installation

To install Drupal, we decided to utilize Composer. First, you will need to download and install composer using the link here: https://getcomposer.org/download/



Afterwards, run the command: `composer create-project drupal/recommended-project my_site_name_dir`



This will download the core Drupal files. 



Follow the Drupal composer installation for more information: https://www.drupal.org/docs/develop/using-composer/using-composer-to-install-drupal-and-manage-dependenciesDependenciesDrupal will need several dependencies to run. These dependencies can be installed using the composer as well. 



Simply run the command on the root directory: `composer install --no-dev`



#### Working with Acquia 

Acquia was built specifically for testing and deploying Drupal websites. After pulling the Git repository codebase, click to **create from local Drupal site.**

When selecting a folder, make sure to select the **web** folder and change the **local site name** to chronica.



![Acquia Setup](C:\Users\itsbh\Documents\GitHub\Chronica\Doc\Images\Acquia Setup.png)