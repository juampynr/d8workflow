# Drupal 8 workflow

This repository contains a Drupal 8 installation which serves as a
sample project for the book "A development workflow for Drupal 8
projects".

## Requirements

* PHP 7.3 or higher.
* Composer 1.7.1 or higher.
* MySQL/MariaDB.
* Apache.

## Installation

1. Create a database:

```bash
mysql --user=root --password --execute="create database 'd8workflow'"
```

2. Download the database dump from [insert URL here]. Then import it
   into the database that you created in step 2:
   
```bash
gunzip d8workflow.sql.gz
mysql --user=root --password --database=d8worfklow < d8workflow.sql
```

3. Clone this repository and install its dependencies:
 
```
git clone git@github.com:juampynr/d8workflow.git
composer install
```

4. Review and adjust the database credentials at `web/sites/default/settings.local.php`.

4. Run `vendor/bin/drush core:status`. Verify that Drupal can
   bootstrap. 

5. Set up the web server so it points to the `web` subdirectory.

6. Execute `vendor/bin/drush user:login` to obtain an admin login URL.
   Adjust the hostname and open it with the web browser.
