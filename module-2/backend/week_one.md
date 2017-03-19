## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
 -GET - retreive information
 -POST - posting new information
 -PUT - updating existing information
 -DELETE - delete information 
 -unsure of 5th
2. What is Sinatra?
  - a DSL for writing web apps in Ruby 
4. What is MVC?
 - model view controller - a framework or outline of how to build out user interface for an application. Controller is where paths are defined, models is where the ruby (or other programming language) logic and database interaction is (in our case with ActiveRecord) and views are the layouts (HTML/CSS) for the actual web pages. 
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
 - so that it is easier to read by others and maintain in the future - they are conventions for a reason, it's what people expect. 
6. What types of variables are accessible in our view templates without explicitly passing them?
  - local variables
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    @name = "Mr. Ed"
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
9. What's the purpose of ERB?
  - allows us to embed dynamic ruby content into html 
10. Why do I need a development AND test database?
  - test databases are always (or should be) wiped clean after each test and populated with given data in the test. Development database populates with given data as well but allows you to work with the database in the views while you are developing the application. 
11. What's responsive design?
  - design that responds to various screen sizes. The elements resize depending on the screen size - from desktop to laptop to tablet to phone
12. What is CRUD and why is it important?
  - Create, Read, Update, Delete - it is the basic funtionality web apps should have - it should be able to create a new object (ex. task) read all tasks and a single task, update a task and delete a task. 
13. What does HTTP stand for? 
  - Hyptertext Transfer Protocol 
14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  -```<%= %> and <% %>``` the first shows the output of the ruby code and the second does not. So if you needed to use an enumerable block you would but the .each block in the second one and what you actually wanted output to the page in the first. 
15. What's an ORM?
  - Object Relational Mapping - a way to connect objects in a programming language to a database
16. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  - ActiveRecord 
17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  get '/restaurants' - gets the list all of the restaurants and displays it
  get '/restaurants/new' - gets the form to create a new restaurant 
  post '/restaurants' - posts a new restaurant to the list of all after submitting the new form 
  get '/restaurants/:id' - gets a specific restaurant information based on the id 
  get '/restaurants/:id/edit' - gets a form that edits the specific restaurant's information based on id
  put '/restaurants/:id' - updates the specific restaurant's information after submitting the edit form
  delete '/restaurants/:id' - deletes the specific restaurant based on id 
  
18. What's a migration? 
  - creates/updates the database schema 
19. When you create a migration, does it automatically modify your database?
  - no, you have to run rake db:migrate
20. How does a model relate to a database?
  - the model is the part of the mvc that interacts/manipulates the data from the database - creates ruby objects from each row in a table in the databse 
21. What's the difference between agile workflow and waterfall method?
  - agile means you do shorter development cycles for individual features and get feedback after each iteration. Waterfall means you plan out the entire development from the begning and the cycle is much longer before you get feedback. 
22. What is the difference between `#new` and `#create`?
  -#new is a new object, but does not save it to the DB until you .save it. #create is new and save together. 
