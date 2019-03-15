# Drupal 8 workflow

This repository contains a Drupal 8 installation which serves as a
sample project for the book "A development workflow for Drupal 8
projects".

## Requirements

* PHP 7.3 or higher
* Composer 1.7.1 or higher
* MySQL/MariaDB
* Apache
* Drush launcher

## Installation

1. Clone this repository and install its dependencies:

```
git clone git@github.com:juampynr/d8workflow.git
composer install
```

2. Review and adjust the database credentials at `web/sites/default/settings.local.php`.

3. Download the database dump from [Insert URL or instructions here].

4. Decompress the database dump, create the database, and import the database dump into it:

```
gunzip d8workflow.sql.gz
drush sql:create
drush sql:cli < d8workflow.sql
```

5. Verify that Drupal can bootstrap with `vendor/bin/drush core:status`.


6. Set up the web server so it points to the `web` subdirectory.

7. Execute `vendor/bin/drush user:login` to obtain an admin login URL. Adjust the hostname and open it with the web browser.
