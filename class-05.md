# Heroku
- **What is Heroku?**

**Heroku** is a container-based cloud Platform as a Service . *Developers* use Heroku to deploy, manage, and scale modern apps. **Heroku** platform is elegant, flexible, and easy to use, offering developers the simplest path to getting our apps to market.    
## Node.js
 - is an **open source**, cross-platform runtime environment, which allows you to build server-side and networking applications. It's written in JavaScript and can be run within the Node.js runtime on any platform.
 - by following  [THIS LINK](https://devcenter.heroku.com/articles/getting-started-with-nodejs) We will know the exact steps to getting Started on Heroku with Node.js
 - **for example** :
   - **Pushing local changes**: 

1. Aftr begin by adding a dependency for ***cool-ascii-faces***   in package.json. Run the following command to do this:
   
                 npm install cool-ascii-faces
                 + cool-ascii-faces@1.3.4
                 added 9 packages in 2.027s
2. Modify index.js so that it requires this module at the start. Also add a new route (/cool) that uses it. Your final code should look like this:

            const cool = require('cool-ascii-faces')
            const express = require('express')
            const path = require('path')
            const PORT = process.env.PORT || 5000

        express()
        .use(express.static(path.join(__dirname, 'public')))
        .set('views', path.join(__dirname, 'views'))
        .set('view engine', 'ejs')
        .get('/', (req, res) => res.render('pages/index'))
        .get('/cool', (req, res) => res.send(cool()))
        .listen(PORT, () => console.log(`Listening on ${ PORT }`)) 

3. Now test locally:

            npm install
            heroku local
   - Visiting your application at http://localhost:5000/cool, you should see cute faces displayed on each refresh: ( ⚆ _ ⚆ ).

4. Now deploy. Almost every deploy to Heroku follows this same pattern. First, add the modified files to the local git repository:

         git add .
5. Now commit the changes to the repository:

        git commit -m "Add cool face API"
6. Now deploy, just as you did previously:

        git push heroku master
7. Finally, check that everything is working:

        heroku open cool
8. we should see another face.