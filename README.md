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


Running app locally
-------------------

Will need to set environment variables for postgres username and password as PG_UN and PG_PW respectively (restart shell after too)

(Or hardcode these details in the config/secrets.yml and just don't commit it... But )

Run server with ```rails s```

When Deploying to Heroku app
----------------------------

Note to self: deployment to Heroku was fine - needed to run ```heroku run rake db:create``` (ignore [PG::ConnectionBad: FATAL:  permission denied for database "postgres"' error)

Then run ```heroku run rake db:migrate```, app error "We're sorry something went wrong" will be resolved

Compile styles before deployment```rake assets:precompile```

Clear cache ```heroku run rake tmp:clear```

Aims to improve app:
--------------------

[ ] Click and drag reordering of tasks

[ ] Give tasks 'levels' depending on priority/urgency of task

[ ] Header navigation bar/images to improve look

[ ] CMS

[ ] Categorise tasks (such as banking/work)

[ ] Add content translation in italian

[ ] Ability to add details to tasks

[ ] Ability to add attachments to tasks

[ ] Adding deadlines to tasks

[ ] Hovering over links - get rid of black background colour

[ ] Hovering over task checkboxes reverts colours/shows inverted font awesome checkbox

[ ] Disable adding tasks if they're empty

[ ] Change mobile design to be more mobile app like (add task button to always be at bottom of page even if task list long?)

[ ] Backlog tasks - if they're not important, be able to hide them in a separate view so task list isn't clogged

[ ] Maybe a points system - assign points to a task so that there is a feeling of achievement when it's completed - more motivation to finish it for user
