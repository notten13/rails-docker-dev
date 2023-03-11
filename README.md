# Rails Docker setup

A very simple setup to work on Rails apps in a Docker container.

## Launch the containers

1. Start the database: `docker-compose up -d mysql`
2. Start the dev container: `docker-compose run --rm -p 3000:3000 rails_dev`

## Create a new Rails app

`rails new . --database db_type`

Create a database and update the database connection options in `config/database.yml`.

## Launch the app

1. Install dependencies: `bundle install`
2. Start the Rails service: `rails server -b 0.0.0.0`

## Create models and migrations

This will generate a model and the corresponding migration:

`rails g model field1:type field2:type ...`

To generate just a migration:

`rails g migration migration_name`

Run migrations:

`rails db:migrate`
