# Apache2 Vhost Macros

This is a collection of vhsot macros that i'm slowly building

You will need to add the following line to your apache config file above where your vhosts are loaded

    # Include macros
    Include <macro folder>

Example installation for Ubuntu 12.04

Clone the Repo

```
git clone https://github.com/hazanjon/apache-macros.git /etc/apache2/sites-macros
```
   
Edit Apache Config

```
vi /etc/apache2/apache2.conf
```
Add the following line

    Include sites-macros/
  
Above the following line

    # Include the virtual host configurations:
    Include sites-enabled/
