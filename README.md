# First Rails App Readme

A test Ruby on Rails app that _will_ be deployed to Heroku to test out building and running a real ruby on rails app. Not meant to be very complex, but hopefully can be some good practice!
# Install 
Use `bundle install` to install the repository.
You'll also need to initialize Postgres, so you can do that with `initd -D ./data`
    Do it locally, because the default folder int `/usr/` doesn't have the correct permissions on my laptop
Then, in order to run the Postgres server, run `postgres -D ./data`
Also, you'll probably need to create the database or else you'll have some tubular issues, you can do that with: `rake db:create` and then `rake db:migrate`.
# Run
Run the command `rails server`. Note: Make sure postgres is running or you'll get some crazy wicked errors.
Notes:
- You'll definitely need to install `rails` too. 
- Make sure to install postgres via gem
- Make sure to install webpacker: `rails webpacker:install`
- Make sure to install yarn: `npm install -g yarn`
* Ruby version
    - TBD
* System dependencies
    - PostegreSQL
* Configuration
    - Nothing special in particular
* Database creation
    - bin/rails db:create
* Database initialization
    - Nothing initialized yet
* How to run the test suite
    - Not sure yet, haven't done it before.
* Services (job queues, cache servers, search engines, etc.)
    - None at the moment.
* Deployment instructions
    - TBD, but will be using Heroku

# Deploying
- You will likely have to explicitly allow for the bin/webpack file to be sent with the deploy. 
- Use this command to get the job done: `git add -f bin/webpack && git push heroku head:master`
- In order to run migrations, do: `heroku run rake db:migrate`
- In order to run scaling, do: `heroku ps:scale web=1`
- In order to check the state of the dyno, do: `heroku ps`
- In order to open the app in a browser, do: `heroku open`
- In order to view heroku logs, do: `heroku logs`
# Your Viewing Pleasure™
