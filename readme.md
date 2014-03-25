wids-site
===========

Intro
-----

This is a site for demonstrating CSRF and XSS vulnerabilities.

PHP has only been chosen as it is widely understood. All web applications need to be mindful of these vulnerabilities, regardless of the language or framework they are created with.

Requirements
------------

- [Heroku account](https://heroku.com/)
- [Heroku toolbelt](https://toolbelt.heroku.com/) installed and ready
- git
- Your favourite text editor

Setup
-----

    git clone https://github.com/arrtchiu/wids-site wids-site
    cd wids-site
    heroku create

    heroku addons:add heroku-postgresql
    
    # You will receive a line of output like:
    # Attached as HEROKU_POSTGRESQL_OLIVE_URL
    # (Yours may be different) - copy the value you got and use it in the next command

    heroku config:set DATABASE_URL=$(heroku config:get HEROKU_POSTGRESQL_OLIVE_URL)

    git push heroku master
    heroku run bin/php www/setup/setup.php

Architecture
------------

This is twitter for cats, called "Meowwer!". It essentially a twitter clone, but with far fewer features.

Site features:

- A user has many posts.
- All posts are public.

User attributes:

- id
- username
- password
- pic_url
- is_admin

Post attributes:

- id
- user_id
- content
