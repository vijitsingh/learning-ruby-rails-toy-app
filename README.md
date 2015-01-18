


Commands ran to build this application : 


-- Setup
- rails new toy_app
- update Gemfile to get the required lib
- bundle install --without production

-- Git
- git init
- git add -A
- git commit -m "Init repo"
- create repo on github using UI
- git remote add origin git@github.com:vijitsingh/learning-ruby-rails-toy-app.git
- git push -u origin master

-- Getting into chapter 1 state
- add a hello def
- update root route in routes.rb

-- deploy to heroku
- git commit -am "Add hello"
- heroku create
- git push heroku master 
- heroku open (https://boiling-citadel-4566.herokuapp.com/)

-- creating User resource
- rails generate scaffold User name:string email:string
- bundle exec rake db:migrate
- rails server # to run the server locally and test (localhost:3000/users , /users/1, /users/new, /users/1/edit)

-- creating Micropost resource
- rails generate scaffold Micropost content:text user_id:integer
- bundle exec rake db:migrate
- add validates :content, length: { maximum: 140 } for max-limit in app/models/micropost.rb
- update app/models/user.rb and micropost.rb to add association.
- rails console
- first_user = User.first
- first_user.microposts
- first_post = first_user.microposts.first
- first_post.user

-- Finishing app
- Commit to git
- git push heroku master
- heroku run rake db:migrate # NOTE THIS COMMAND
- heroku open 

DONE. 
