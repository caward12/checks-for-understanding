## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
  - rails new ProjectName (and then any options - rails version, removing test folder etc) 
2. What do Models generally inherit from in rails?
  - ActiveRecord::Base
3. What do Controllers generally inherit from in a rails project?
  - ApplicationController 
4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
  - get '/horses/:id', to: 'horses#show', as: 'horse' OR resources :horses, only: [:show]
5. What rake task is useful when looking at routes, and what information does it give you?
  - rake routes, give you all route information including prefix, verb, URI patter and controller#action
6. What is an example of a route helper? When would you use them?
  - horses_path or horse_path(horse)
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
  - url provides the full path (localhost:3000/horses) and path provides the local path (/horses)
8. What are strong params and why are the necessary?
  - strong params are defined in a private method in the controller and define what parameters are allowed through in the url especially helpful for forms (create & update) 
9. What role does `form_for` play in helping us create our forms?
  - builds the form for the specific object(s) passed in
10. How does `form_for` know where to submit the user's input?
  - the form_for does some magic behind the scenes when building the form and it checks if the object passed in is a new record or not - if it is, then it knows it is a create form, if it's an exising record then it knows it's an update form. 
11. Create a form using a `form_for` helper to create a new `Horse`. 
  ``` <%= form_for @horse do |f| %>
        <%= f.label :name %>
        <%= f.text_field :name %>
        <%= f.submit %>
       <% end %> 
 ```
       
12. Why do we want to validate our models?
  - we want to make sure that information necessary to create the object is present when creating/editing and/or that fields that need to be unique are indeed unique. 
