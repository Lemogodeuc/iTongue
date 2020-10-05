## Step 1: Install dependencies

To run this project please follow thoose steps:

- first clone it into a local folder of yours
- open it in your favourite editor
- open a new terminal and hit command:

```bash
npm install
```

---

## Step 1: Install database

This project uses [PostgreSQL](https://www.postgresql.org/) so it assumes that you have a minimum knowledge with [SQL](https://sql.sh/) language and be confortable with PostgreSQL.

To be able to use Aryon, please follow thoose steps:

- [Create a new role](https://www.postgresql.org/docs/12/sql-createrole.html) WITH LOGIN and give it whatever password you want. Keep it in mind or write it somewhere, you'll need it quickly again.

Example:

```SQL
CREATE ROLE "itongue" WITH LOGIN 'GjqS.jDVxUBGv6*+';
```

- [Create a new database](https://www.postgresql.org/docs/12/sql-createdatabase.html) and set the owner to be the role previously created.

Example :

```SQL
CREATE DATABASE "itonguedb" OWNER "itongue";
```

You know have a new database to work with.

---

## Step 3: Prepare your migrations

To work easily with the database, this project uses [Sqitch](https://sqitch.org/) to manage all migrations. You can follow previous link to install it and learn quickly how to work with it.

Once installed (and the tutorial followed), open a new terminal (or with the one you have already open), navigate to be on the root folder if you are somewhere else.

Once done, please create a new file in the root folder called `sqitch.conf` and copy-past the code you have in the `sqitch-example.conf` file. Then, replace `<DATABASE_ROLE>`, `<DATABASE_PASSWORD>` and `<DATABASE>` by yours.

To make sure everything is fine, you can run in your terminal the command:

```bash
sqitch deploy
```

---

## Step 4: Run the project

You can now run the project using

```bash
npm run dev
```

Enjoy 🚀

---

## Technologies

This project uses several technologies. You can reach the documentation for any of them following their links.

### Environment

- [Node](https://nodejs.org/en/) - JavaScript runtime built on [Chrome's V8 JavaScript engine](https://v8.dev/)
- [Dotenv](https://www.npmjs.com/package/dotenv) - Loads environment variables from your `.env` file into `process.env`
- [Cors](http://expressjs.com/en/resources/middleware/cors.html) - Middleware used to enable [CORS](https://en.wikipedia.org/wiki/Cross-origin_resource_sharing) with various options

### Database and migrations

- [Postgresql](https://www.postgresql.org/) - This is your [database management system](https://en.wikipedia.org/wiki/Database#Database_management_system)
- [Pg](https://www.npmjs.com/package/pg) - Known as a _non-blocking PostgreSQL client for Node.js_, you'll find the official documentation [here](https://node-postgres.com/)
- [Sqitch](https://sqitch.org/) - Will be your best friend to manage your migrations

### Cache

- [Redis](https://redis.io/) - In-memory data structure store

### Server

- [Express](https://expressjs.com/) - Web framework (v.4)

### Validation

- [Express validator](https://express-validator.github.io/docs/) - Middlewares wrapping Validator.js

### Client-Server communication

- [Json Web Token](https://www.npmjs.com/package/jsonwebtoken) - An implementation of JSON Web Tokens.
- [Socket.io](https://socket.io/) - Provides bi-directional communication channel between a client and a server for the chat system.
- [Multer](https://www.npmjs.com/package/multer) - Middleware for handling multipart/form-data

### Documentation

- [Swagger](https://swagger.io/) - API documentation management

### Encryption

- [Bcrypt](https://www.npmjs.com/package/bcrypt) - Allow you to hash strings

### Utils

- [Nodemon](https://www.npmjs.com/package/nodemon) - Automatically restarting the node application when file changes.
- [Slugify](https://www.npmjs.com/package/slugify) - Slugify strings
- [Morgan](https://www.npmjs.com/package/morgan) - HTTP request logger middleware for node.js
