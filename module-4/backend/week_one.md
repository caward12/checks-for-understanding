## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's the most useful thing you learned from completing the intermission week work?
- basic javascript - for loops, forEach, functions, difference between objects in js and hashes in ruby

2. What are some tools to help debug JavaScript code?
- pry.js, console.log

3. What are some tools you need in order to unit test your JavaScript?
- mocha and chai 

4. What is the syntax for invoking a function?
functionName()

5. What's the difference between `==` and `===` in JavaScript?
- == checks if something is equal to something else, not strict. Example: 2 == 2 //true or true == 1 //true
- === checks if something is equal to something else, is strict, meaning it also checks the datatypes Example: true === 1 //false because true is a boolean and 1 is an integer

6. What's the difference between asynchronous and synchronous JavaScript? 
- asynchronous - does not wait for a function to finish before moving on to the next. 
- synchronous - does wait for a function to finish before moving on. 

7. How do we setup a route when creating an API with Node and Express?
- in the server.js file set var app = Express() then you can set app.get or app.post and pass in the url and tell it what to response with (response code and/or some data via a query to the database) 

8. What do we use Knex for?
- setting up/connecting to the database from node/express - create/run migrations, seeds

9. What's `npm` and what do we use it for?
- node package manager - it's somewhat equivalent to a "gem" manager in ruby - helps you install pagackges for node and run them from the command line. 

#### Review  
10. What's the MVC design pattern? Describe each part of MVC?
- Model, view, controller. When a request is made, it first hits the routes file (or server file in js) and that is then directed to the specified controller and action. That controller action then returns data based on the code in the controller and gets it from the model and then passes that data on to the view
  
  Model - where code that interacts with the database lives - class that holds behavior for a given object - either based on a table in the database or as a PORO(in ruby). 
  
  View - where the views - .html files live. Code that displays what shows to the user in the browser. 
  
  Controller - where code that connects the routes to the model to pass data to the view.
  
11. What is AJAX? What are some benefits of using AJAX?
- Asynchronous javascript and XML - can make requests to a server and serve data up in JSON (or XML/HTML or text I believe)

12. What's a background worker? When would we want to use a background worker?
- they are methods that are performed in the background. Ruby typically is synchronous and with background workers it can be asychronous. Example: when a user provides email address and you want to send them an email. When they hit enter, a background worker will do the work to send the email while the user can continue to use the site and not have to wait for the email to be sent. 
