# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

######
#https://gist.github.com/mrilikecoding/9520502#file-gistfile1-txt-L14
\curl -sSL https://get.rvm.io | bash -s stable --ruby

/bin/bash --login

rvm use "version"

rvm use --create version@nameproject

gem install rails

# if using postgres

rails new nameproject --database=postgresql

cd nameproject

rvm --rvmrc version@nameproject

# credentials for railsapp
config/database.yml

rake db:create
rake db:migrate
rake db:seed or setup # go to docs rails

rails s

#add ruby version to gemfile
ruby "version"

bundle install

# gem 'devise'
rails generate devise:install
~> Configure: config/enviroments/development.rb
   app/views/layouts/application.html.erb

# devise "important" ~> cancancan
rails g devise User

rake db:migrate

# create roles users for rails app
# Eg.
rails generate migration add_roles_to_users super_admin_role:boolean admin_role:boolean collaborator_role:boolean user_role:boolean

# add defaults: false, true roles
db /migrate/2019########user.rb

# gem 'rails_admin'
rails generate rails_admin:install

config/initializers/rails_admin.rb # edit for canacancan

# gem 'cancancan'
rails g cancan:ability

app/models/ability

# MVC app ~> scaffold
# eg.
rails generate scaffold Emap name:string description:string country:string type_sys:string latitude:decimal longitude:decimal capacity:int

app/controllers/name_controller.rb # ~> basic configurations

rake db:migrate

rails generate controller Home index

app/views/home/index.html.erb

