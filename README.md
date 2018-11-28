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


# Steps

* 1: Create a set of pages: rails g controller Pages home

* 2: Set the routes accordingly: config/routes, root to: 'pages#home'

* 3: Implement devise: Add Gemfile, bundle install, rails g devise:install, rails g devise:views

* 4: Generate User model using devise. rails generate devise User, rake db:migrate

* 5: Add "omniauth-provider" gems and bundle install

* 6: Rails g migration AddOmniauthTo Users provider:string uid:string name:string image:text

* 7: Update initializer: config.omniauth:facebook, "APP_ID", "APP_SECRET"

* 8: Links to get client_id and client_secret

     https://developers.facebook.com
     https://console.developers.google.com
     https://developer.twitter.com
     https://github.com/settings/application
     https://www.instagram.com/developer/clients/manage
     https://developers.snapchat.com/api/docs

* 9: Keep in mind that emails have to be unique per user, meaning if a user has logged in with one of the sns services already, he can't log in with the same email using another sns service

* omniauth:
  facebook:
    client_id: client_id here
    client_secret: client_secret here
    callback_url: http://localhost:3000/users/auth/facebook/callback

* Put this into rails credential:edit file

* [tutorial on how to do this:](https://www.engineyard.com/blog/rails-encrypted-credentials-on-rails-5.2)
