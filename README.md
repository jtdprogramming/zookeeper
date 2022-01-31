# zookeeper

# You can use the `-y` flag to skip the package questionnaire and leave default answers
npm init -y
# You can use `npm i` as a shortcut for `npm install`
npm i express

# 1.5
There are two important takeaways from this code:

The first is that the get() method requires two arguments. The first is a string that describes the route the client will have to fetch from. The second is a callback function that will execute every time that route is accessed with a GET request.

The second takeaway is that we are using the send() method from the res parameter (short for response) to send the string Hello! to our client.