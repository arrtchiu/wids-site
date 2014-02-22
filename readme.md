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
    git add .
    git commit -m 'update database config'
    git push heroku master
    cat setup/init_db.sql | heroku pg:psql

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
