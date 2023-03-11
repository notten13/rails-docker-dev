# Rails Docker setup

A very simple setup to work on Rails apps in a Docker container.

## Launch the app

1. Start the database: `docker-compose up -d mysql`
2. Start the dev container: `docker-compose run --rm -p 3000:3000 rails_dev`
3. Install dependencies: `bundle install`
4. Start the Rails service: `rails server -b 0.0.0.0`
