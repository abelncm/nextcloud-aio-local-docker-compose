# Run Nextcloud AIO (All In One) In Your Localhost

I created this docker compose file for those who want to easily run this project in their localhost.

I wanted to help a lost soul in this endevour since the official documentation may get a little confusing. 

I believe this configuration simplifies everything.

Original repository: https://github.com/nextcloud/all-in-one


## Run

Edit hosts file (linux example)

    sudo vi /etc/hosts

Add this:

    127.0.0.1   local.docs

In project directory

    docker compose up

Or when making changes to the docker compose file

    docker compose up --build

Go to the page conclude installation

    https://local.docs:8080


After everything is installed it will give you the credentials for you to login in

    https://local.docs


#### Observations

Caddy is used as reverse proxy since Nextcloud AIO depends on a domain name to work.
Caddy is also responsible for generating the internal TLS certificate using Let's Encrypt. This is all done automatically.

If you want to use another domain name just edit your hosts file and the Caddyfile.
