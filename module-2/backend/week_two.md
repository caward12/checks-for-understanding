## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
  - ActiveRecord is what allows us to create ruby objects from databases and make queries on the database- it is an ojbect relational mapper. 
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
  - you can call all, count, find, find_by, where. These methods are accessible because we are extending from ActiveRecord and they are ActiveRecord methods.  

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
  - Team.find(4).name
  - Team.find(4).owner_id

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
  - Team.find(4).owner

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
  - the relationship between students and teachers would be many to many - a student has many teachers and a teacher has many students. (assuming this is any school setting other than elementry school) There would be one table for student, one table for teacher and then a join table that has columns for its own primary key, student_id and teacher_id that would both be foriegn keys. a
6. Define foreign key, primary key, and schema.
  - foreign key: is a column on another table that uniquely identifies another row on a other table. 
  - primary key: is the column that is unique for every record in that table
  - schema: defines how the tables in a database relate to eachother and how those tables are set up - what columns and datatypes those columns are. 
7. Describe the relationship between a foreign key on one table and a primary key on another table.
  - a foreign key on one table is the primary key that uniquely identifies a row on another table. For example: you have one table "Bikes" that say has a row with an ID of 2 and a bike number of 23. On the "Trips" table you would have a column called bike_id that might have 2 in a row. This 2 is the primary key of the bike numbered 23 and uniquely identifies that bike on the bikes table. 
8. What are the parts of an HTTP response?
  - an HTTP response includes status code (2xx, 3xx, 4xx or 5xx), content length and html


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do. 
  - all - returns all of the records for that table
  - count - returns the number of records in that table
  - find() - returns the object/record that matches the id in the ()
  - find_by() - allows you to search for objects by column names other than id - but only returns the first matching record
  - where() - similar to find_by() but will return all matching records. 
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
  - rake db:create_migration - creates the migration file to create/edit a table
  - rake db:environment:set/rake db:test:prepare - make it so when you run your test it is using the correct environment database - test
  - rake db:migrate - runs migration files to create/edit table in database
3. What two columns does `t.timestamps null: false` create in our database?
  - created_at and updated_at
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
  - one to many (a school has many teachers but a teacher only has one school)
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
  - you will need to add a column school_id to the teachers table - which is a foreign key pointing to the primary key on the schools table. 
6. Give an example of when you might want to store information besides ids on a join table.
  - if the relationship results in other attributes. for example in a join table of Students and Courses you might have a column for grade because you get a grade when a student takes a course
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?
