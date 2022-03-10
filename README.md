# Node.js Weight Tracker connect to servers

This sample application demonstrates the following technologies.

* [hapi](https://hapi.dev) - a wonderful Node.js application framework
* [PostgreSQL](https://www.postgresql.org/) - a popular relational database
* [Postgres](https://github.com/porsager/postgres) - a new PostgreSQL client for Node.js
* [Vue.js](https://vuejs.org/) - a popular front-end library
* [Bulma](https://bulma.io/) - a great CSS framework based on Flexbox
* [EJS](https://ejs.co/) - a great template library for server-side HTML templates

**Requirements:**

* server connection with sshkey, ip addres amd userName
* [Node.js](https://nodejs.org/) 14.x
* [PostgreSQL](https://www.postgresql.org/) (can be installed on server using Docker)
* [Free Okta developer account](https://developer.okta.com/) for account registration, login
* [pm2] (https://pm2.keymetrics.io/)
## Install and Configuration - web application

1. connect to the server ubuntu with your sshkey using userName@ipadress 
1. Clone source files from Github to the server
1. Run `npm install` to install dependencies (need to be installed on the server)
1. create with [nano] file for your [.env] -
1.  inside your .env file you need to add PostgreSQL connection - using PostgreSQL ip adress
1.  change your HOST_URL adding the app external ip to connect
1.  Create a [free Okta developer account](https://developer.okta.com/) and add a web application for this app
1.  Copy `.env.sample` to `.env` and change the `OKTA_*` values to your application , inerst your okta client id + client secret .
             [do not forget to add .gitignore file for your .env && node_modules]
1. install and update [node.js --v 14] on your server 
1. install pm2 - to stay connected to the server.


## Install and Configuration - data base
1. connect to the server ubuntu with your sshkey using userName@ipadress 
2. install docker and PostgreSQL on your data base server.
3. create docker container using [--restart unless-stopped] command - for the server to stay connected 
4. you can run [docker ps] - to see that you actually connected to PostgreSQL.

## back to your web server
6. Initialize the PostgreSQL database by running `npm run initdb` - ## on your web server
7. Run `npm run dev` to start Node.js 
 

The associated blog post goes into more detail on how to set up PostgreSQL with Docker and how to configure your Okta account.
1. If you don't already have PostgreSQL, set up using Docker
