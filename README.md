Goal of the homework
--------------------
Install and set-up Ruby, Rails, Git, and Heroku.
Then deploy a basic Rails app on Heroku.

Issues I ran in to
------------------

Wanting to use a tool like virtualenv for Ruby, so I found RVM and set it up using the following tutorial:
https://www.digitalocean.com/community/articles/how-to-install-ruby-on-rails-on-ubuntu-12-04-lts-precise-pangolin-with-rvm

Wanting to set up and use a different heroku account to deploy to other than the one I currently have set up on my machine, so I ended up using the heroku-accounts tool and followed this tutorial:
http://railsware.com/blog/2013/02/05/how-to-set-up-the-heroku-tools-for-deployment-with-multiple-accounts/

Then I used the following tutorial on Heroku's blog to figure out how to allow sqlite to be run on my machine while using postgres on Heroku*:
https://devcenter.heroku.com/articles/getting-started-with-rails4


* This turned out to be a lot harder than I expected since you not only had to change the Gemfile to install postgres for Production and sqlite for Development (since heroku would throw a fit if you tried to install sqlite with postgres on Production), but you had to change the database file to use the sqlite engine for Development and postgres engine for Production then delete the username from the Production database settings.





