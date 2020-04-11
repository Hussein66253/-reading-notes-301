
# Embedded Javascript
- ***EJS*** stands for **Embedded Javascript**. It is a simple templating language/engine that lets its user generate HTML with plain javascript.  It also helps to embed JavaScript to HTML pages. 
- To begin with, using EJS as templating engine we need to install EJS using given command: 

         npm install ejs
              or
        npm install ejs --save.  
## EJS tags 
1. **<%= %>** : Prints value For examples:

    - <%= 2 + 2 %> prints out 4.
    - 
    1. in a app.js file

            var express = require('express');
            var ejs = require('ejs');
            var app = express();
            app.set('view engine', 'ejs');

            app.get("/", function(req, res) { // root route or home route
                res.render("home", {
                    x: "Lucy Christ",
                    age: 16
                });
            });
            app.listen(3000, function() {
                console.log("server is listening!!!");
            });

            
                
        2. in a index.html file

                <h1>Hello, my name is <%=x%> and i am <%=age%> </h1>
        3. The view on port in a browser *localhost:3000*

             ![EJS RESULT](https://www.includehelp.com/node-js/Images/ejs-variables-1.jpg "EJS RESULT FOR VALUES")



2. **<% %>** : is used to include some programming methods we want to use. Like If/else and loops.

        <h1>Hey <%= username.toUpperCase() %>, Welcome to Our site</h1>
        <% if(username.toLowerCase() === "danny"){ %>
        <p>Danny you are Beautiful!</p>
        <% } else { %>
        <p>You are not Danny, you are not Beautiful!</p>
        <% } %>

     - The view on port in a browser *localhost:3000*

        ![EJS RESULT](https://www.geeksread.com/wp-content/uploads/2018/06/Cnditional-statement-ejs_1.jpg "EJS RESULT FOR LOOP")

    

