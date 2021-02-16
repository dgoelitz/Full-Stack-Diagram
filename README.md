-Major Systems: Client, Server, Database.
--Client
The client is where we house the application itself. The client system is what the user will interact with. All of the raw functionality of the application lives here. We may also have a css file here to give style to the layout of our application. The client and server work together by having their links called in html. As described below, we have a few options in our toolbelt for how we create the html on our page.


--Server
The server stores the information that we want available between the user's sessions with the client. For example, if we had a cookie stored in the server, then the user can continue their session in the browser after they have closed the window and reopened it at another time. We will use express to help us with cookies. For our cookies, we will also need middleware. Middleware is kept on the server side. One piece of middleware we will need is a cookie parser to properly read our cookies. Our html that calls all of the scripts together and describes what will be printed to the screen is also in the sever side. It uses ejs files with express. Alternatively, we could have an html file for the contents of our page. We will likely create html dynamically as well, using react.


--Database
This is where we will house our database containing any tables that we need for our program. We can create our tables with a promise chain using bluebird. That way each table will be created one at a time after the previous table has been initialized. We should export our database with module.exports from node.js. Then, we can make use of the database in our server. For the database itself we will use mysql.