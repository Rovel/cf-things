## Things App
This app is just a bare bones Rails app to test our CloudFormation stack.

## Requirements

* Docker
* Ruby 2.3
* You must have a [Docker Hub](http://hub.docker.com) account

## Procedure

1. `bundle install`
2. `docker-compose up` will bring up the app locally
3. `docker-compose exec web rails db:create` will create the db
4. `docker-compose exec web rails db:migrate` will migrate the db

You can now check out the app at http://localhost:3000

If it all looks good, you can build and push to your Docker Hub account.

    docker build . -t dh-account/cf-things
    ... Wait for build ...
    docker push dh-account/cf-things

Replace `dh-account` with your Docker Hub account name.
