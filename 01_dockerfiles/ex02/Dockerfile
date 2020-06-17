FROM ruby
RUN apt-get update
RUN apt-get install -y nodejs sqlite3 yarn
#maybe?
RUN rm -rf /var/lib/apt/lists/*
RUN gem install rails
#probably ONBUILD
#rails application inside directory?
ONBUILD COPY rails_app /opt/app
#probably ONBUILD
ONBUILD WORKDIR /opt/app
#check if this works
ONBUILD RUN bundle install
ONBUILD RUN rails db:migrate
