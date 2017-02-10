**How to use**

* Just run in app rails root directory

`sudo docker run -it --name app --rm --user "$(id -u):$(id -g)" -p 3000:3000 \
-v "$PWD":/usr/src/app -w /usr/src/app ederrogersouza/rails-5-ruby-2.4 gem update --system && \
bundle install && rake db:create && rake db:migrate && rspec && rails s`
