# SQLDM Music Tour API

In this project we will be working with a database and APIs.

# The files and folders

## The file structure follows the MVC structure we learned about in course 6, minus views since we are creating an API.

/controllers folder - Where we will house all our endpoint routes that interact with the database
/models folder - Where we will write out our tables and columns
server.js - Our entry file, where most server configuration is housed.
.env - Our environment variables; It is recommended that you add it into the .gitignore file.

# server.js

## Again, it has been a little while since we worked with Express. So let's briefly break down each section.

Dependencies - Where we require all our packages
Configuration/Middleware - Where we configure those dependency packages
express.json() and express.urlencoded(...) - Configuration for body-parser, which parses request bodies that come in
Root - A GET for the root route ('/'), responding with a simple welcome message
Listen - Where we tell our app what port to listen for connections on

# Dependencies

npm i
npm i sequelize
npm i pg pg-hstore
npm i -g sequelize-cli
sequelize init:config
sequelize init:models
sequelize init:migrations
sequelize model:generate --name Band --attributes "band_id:integer, name:string, genre:text, available_start_time:date, end_time:date" --force true
sequelize db:migrate
