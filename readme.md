widc-sploit
===========

Requirements
------------

- [Heroku account](https://heroku.com/)
- [Heroku toolbelt](https://toolbelt.heroku.com/) installed and ready
- git
- Your favourite text editor

Setup
-----

    git clone https://github.com/arrtchiu/widc-sploit widc-sploit
    cd widc-sploit
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
