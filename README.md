# Apache2 Vhost Macros

This is a collection of vhsot macros that i'm slowly building

You will need to add the following line to your apache config file above where your vhosts are loaded

    # Include macros
    Include <macro folder>/*.conf

## Usage

Add the following to your vhost file

```
Use generic mydomain.com
```

This will create a vhost that serves up /var/www/mydomain.com on port 80


## Example installation for Ubuntu 12.04

### Clone the Repo

```
git clone https://github.com/hazanjon/apache-macros.git /etc/apache2/sites-macros
```

### Enable Macros in Apache
```
apt-get install libapache2-mod-macro
a2enmod macro
/etc/init.d/apache2 restart
```

### Edit Apache Config

```
vi /etc/apache2/apache2.conf
```

At he bottom of the config file add

    Include sites-macros/*.conf
  
Above the following line

    Include sites-enabled/
    
### Reload Apache
```
/etc/init.d/apache2 reload
```

