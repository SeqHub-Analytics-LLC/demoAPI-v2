Login to heroku with ```heroku login```

Set up package.json first with: ``` npm init ```

Create index.js ``` touch idex.js ```

To run, ``` node index.js ```

Install express and other dependencies:
```
# to use nodemon anywhere on computer:
npm install -g nodemon
# to install libraries in project directory
npm install mongodb express body-parser cors --save
```
Note: body-parser takes input from requests and provides ways to use them. cors allows you to access resources cross-domain. cors is not super necessary for this particular api as there will not be any frontend for now.  

Use postman to test out sending requests. Note that when you do POST or DELETE, select body - raw, and then write a json data etry. Click into 'code', make sure that the cotent type is application/json. 

We want to model our data so that our data has the same structure (schema) across apps. This is when mongoose comes in. Run the following to install dependencies. (mongodb-uri) is used so that we can connect to mongodb. 
```
npm install mongoose mongodb-uri --save
```
Schema is in api/demoEntries/model/demoEntry.js

At this point, I've also created an app on heroku with 
```
heroku create test-api-615
# now add mongodb
heroku addons:create mongolab
```

Go to heroku website, enter our app test-api-615, click on mongodb addon to access mLab website. Under Users, create a new user with credentials: 
```
username: user
password: p123456
```

Installed mongodb community edition with homebrew. 
```
brew tap mongodb/brew
brew install mongodb-community@4.2
```
You can use the mongo shell credentials on mongodb to access the database through command line.

6/18
About to a functionality that lets researchers create collections on mongodb and connect with that collection.
 

