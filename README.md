# laravel-dev-env
Build a development environment for laravel

## Prerequisites
### Docker
Add this line in /etc/hosts :<br>
`127.0.0.1 laravel-dev-env.localhost`
Or configure laravel-dev-env/docker/nginx/laravel.conf, line 2 :
`server_name laravel-dev-env.localhost`
The important thing is that the two names in this two files must match.

### Laravel Project
Then create your laravel project named 'laravel' by using this command :
`composer create-project laravel/laravel laravel`
You need to install composer first : https://getcomposer.org/download/

## Launch you app
To launch your app, you need to execute this command :
`docker-compose build && docker-compose up -d`
Once this command executed, your site is available here : http://laravel-dev-env.localhost:8080 (depending on what you choose in Prerequisites - Docker section.

## Troubleshooting
You might have a permission error on storage directory. To correct it :
`docker-compose exec php chmod 777 -R storage`
