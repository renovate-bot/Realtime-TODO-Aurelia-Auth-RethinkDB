A Realtime TODO App with [Aurelia](http://aurelia.io), [Socket.IO](http://socket.io/), [Node.js](http://www.nodejs.org/), [Koa](http://koajs.com/) and [RethinkDB](https://www.rethinkdb.com/) and [WebSockets](https://developer.mozilla.org/en/docs/WebSockets).

A summary of tech stack:
* **Client**: Aurelia and Twitter Bootstrap.
* **Server**: Koa for RESTful API serving on Node.js.
* **Socket.IO** along with JSON-RPC is used for real-time client-server communication and browser sync.
* **RethinkDB** as our database.

## Getting Started
Make sure that you have Node.js v4 or higher, and RethinkDB v3 or higher (running on the default port 28015) installed on your computer. To get started, do the following:

######Server
```bash
git clone https://github.com/ghiscoding/Realtime-TODO-Aurelia-RethinkDB
cd Realtime-TODO-Aurelia-RethinkDB
npm install
npm start
```

######Client
```bash
cd Realtime-TODO-Aurelia-RethinkDB/client
npm install
npm run dev
```

Your application should run on the 4081 port so in your browser just go to [http://localhost:4081](http://localhost:4081).

## Database (RethinkDB)
You will need to create a `Test` database with a `todos` table. Running the project and adding a new Todo, should in theory, create the table structure.

If you want to use the login credentials, you will need to create a `users` table under the `test` database. The table structure is `{ id, mail, password, username }`. You also need to go in `client/src/main.js` and uncomment the code `let root = auth.isAuthenticated() ? 'app' : 'login';` to activate the logins (you can remove the other line `let root = 'app';`).

## Configuration
######Client
All configuration is specified in the [/client/src/config](https://github.com/ghiscoding/Realtime-TODO-Aurelia-RethinkDB/blob/master/client/src/config.js) directory, particularly the [config.js](https://github.com/ghiscoding/Realtime-TODO-Aurelia-RethinkDB/blob/master/client/src/config.js) file.

######Server
All configuration is specified in the [/server/config](https://github.com/ghiscoding/Realtime-TODO-Aurelia-RethinkDB/blob/master/server/config.js) directory, particularly the [config.js](https://github.com/ghiscoding/Realtime-TODO-Aurelia-RethinkDB/blob/master/server/config.js) file.

## License
MIT
