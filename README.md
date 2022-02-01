# zookeeper
Key notes and code snippets for studies
# You can use the `-y` flag to skip the package questionnaire and leave default answers
npm init -y
# You can use `npm i` as a shortcut for `npm install`
npm i express

# 1.5
There are two important takeaways from this code:

The first is that the get() method requires two arguments. The first is a string that describes the route the client will have to fetch from. The second is a callback function that will execute every time that route is accessed with a GET request.

The second takeaway is that we are using the send() method from the res parameter (short for response) to send the string Hello! to our client.

# 2.5
First, we used the app.use() method. This is a method executed by our Express.js server that mounts a function to the server that our requests will pass through before getting to the intended endpoint. The functions we can mount to our server are referred to as middleware.

Middleware functions can serve many different purposes. Ultimately they allow us to keep our route endpoint callback functions more readable while letting us reuse functionality across routes to keep our code DRY.

The express.urlencoded({extended: true}) method is a method built into Express.js. It takes incoming POST data and converts it to key/value pairings that can be accessed in the req.body object. The extended: true option set inside the method call informs our server that there may be sub-array data nested in it as well, so it needs to look as deep into the POST data as possible to parse all of the data correctly.

The express.json() method we used takes incoming POST data in the form of JSON and parses it into the req.body JavaScript object. Both of the above middleware functions need to be set up every time you create a server that's looking to accept POST data.

# 3.4
```
app.use(express.static('public'));
```

We added some more middleware to our server and used the express.static() method. The way it works is that we provide a file path to a location in our application (in this case, the public folder) and instruct the server to make these files static resources. This means that all of our front-end code can now be accessed without having a specific server endpoint created for it!