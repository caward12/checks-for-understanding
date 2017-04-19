## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie? a small piece of data stored on the browser
* What’s the difference between a session and a cookie? sessions are stored on the server side, cookies are store in the browser. They both allow websites to remember "state" since HTTP requests are stateless
* What’s a flash and when do you want to use flashes? flashes are messages that notify the user that something happened - you want to use them to let the user know they successfully did something, or if something went wrong when they were trying to do something. 
* Why do people say “HTTP is stateless”? HTTP does not remember any previous requests
* What’s authentication? Explain. Authentication is checking to see if a user's credentials (username/password) match those in the database and so they are authenticated to log in to the application. 
* What’s the difference between authentication and authorization? Authentication is checking to see if a user is an exisitng user in the database. Authorization is checking if the user is authorized to view certain pieces of content or parts of an application - this is usually dependant on the user's role in the database. 
* What’s a before filter? before actions are things that happen before whatever action you define - so if you say before_create then the code would execute before the create method is called. if you just say before_action, then the code is executed before anything else. 
* How do we keep track of a user once they’ve logged in? sessions - set current user through sessions[:user]
* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches? namespace is best when the content is related to authorization - so an admin can only view the content. Nesting resources is best when there is a relationship between the content so for example jobs belong to a certian company so you would see the jobs for a particlar company. 
* At a high level, what tools can you use to implement authorization? How would you use them? Adding roles to users, adding an enum to the user model, setting current_user through session and then current_admin to see if they are an admin (via role). You could also use Oauth through a different site - twitter, facebook, github etc. 
* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum? An enum is a method that converts integers to strings. Most often seen in users for role - data needs to be an integer in the database. You put the enum in the model. the use of an enum allows you extra methods, so if you have an enum that defines user and admin, then instead of checking if they have a role of 0 or 1, you can call .admin? to see if they are an admin. 
* What are some strategies you can use to keep your views DRY? You could use partials; write methods in the model
