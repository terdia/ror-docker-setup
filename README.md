# ror-docker-setup
Docker setup for local development with Ruby on Rails 

## Setup

1. docker-compose build 
2. docker-compose up -d
3. docker-compose run web bash 

## Install Ruby on Rails 
1. rails new . --force --database=postgresql
2. bundle install
3. yarn install

## Update config/database.yml like so

```
default: &default
  adapter: postgresql
  encoding: unicode
  # For details on connection pooling, see Rails configuration guide
  # https://guides.rubyonrails.org/configuring.html#database-pooling
  pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>
  host: db
  username: postgres
  password: password
```

## Next 
1. rake db:create
2. rake db:migrate

Navigate to http:/localhost:3000 
