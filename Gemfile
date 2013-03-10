source 'https://rubygems.org'

ruby '1.9.3'

gem 'active_model_serializers', git: 'git://github.com/rails-api/active_model_serializers.git'
gem 'ember-rails', git: 'git://github.com/emberjs/ember-rails.git' # so we get the pre version
gem 'vestal_versions', git: 'git://github.com/zhangyuan/vestal_versions'

gem 'message_bus', path: 'vendor/gems/message_bus'
gem 'rails_multisite', path: 'vendor/gems/rails_multisite'
gem 'simple_handlebars_rails', path: 'vendor/gems/simple_handlebars_rails'

gem 'redcarpet', require: false
gem 'activerecord-postgres-hstore'
gem 'acts_as_paranoid'
gem 'active_attr' # until we get ActiveModel::Model with Rails 4
gem 'airbrake', '3.1.2', require: false # errbit is broken with 3.1.3 for now
gem 'clockwork', require: false
gem 'em-redis'
gem 'eventmachine'
gem 'fast_xs'
gem 'fast_xor'
gem 'fastimage'
gem 'fog', require: false
gem 'has_ip_address'
gem 'hiredis'

# note: for image_optim to correctly work you need
# sudo apt-get install -y advancecomp gifsicle jpegoptim libjpeg-progs optipng pngcrush
gem 'image_optim'
gem 'jquery-rails'
gem 'minitest'
gem 'multi_json'
gem 'mustache'
gem 'nokogiri'
gem "omniauth"
gem "omniauth-openid"
gem "openid-redis-store"
gem "omniauth-facebook"
gem "omniauth-twitter"
gem "omniauth-github"
gem "omniauth-browserid", :git => "git://github.com/callahad/omniauth-browserid.git", :branch => "observer_api"
gem 'oj'
gem 'pg'
gem 'rails'
gem 'rake'
gem 'redis'
gem 'redis-rails'
gem 'rest-client'
gem 'rinku'
gem 'sanitize'
gem 'sass'
gem 'seed-fu'
gem 'sidekiq'
gem 'sinatra', require: nil
gem 'slim'  # required for sidekiq-web
gem 'therubyracer', require: 'v8'
gem 'thin'
gem 'diffy'
gem 'autoscaler'
gem 'dalli'

# Gem that enables support for plugins. It is required.
gem 'discourse_plugin', path: 'vendor/gems/discourse_plugin'

# Discourse Plugins (optional)
# Polls and Tasks have been disabled for launch, we need think all sorts of stuff through before adding them back in
#   biggest concern is core support for custom sort orders, but there is also styling that just gets mishmashed into our core theme. 
# gem 'discourse_poll', path: 'vendor/gems/discourse_poll'
gem 'discourse_emoji', path: 'vendor/gems/discourse_emoji'
# gem 'discourse_task', path: 'vendor/gems/discourse_task'

# Gems used only for assets and not required
# in production environments by default.
# allow everywhere for now cause we are allowing asset debugging in prd
group :assets do
  gem 'sass'
  gem 'sass-rails'
  gem 'turbo-sprockets-rails3'
  gem 'uglifier'
end

group :test do
  gem "fakeweb", "~> 1.3.0"
end

group :test, :development do
  gem 'jshint_on_rails'
  gem 'guard-jshint-on-rails'
  gem 'certified'
  gem 'fabrication'
  gem 'guard-jasmine'
  gem 'guard-rspec' 
  gem 'guard-spork'
  gem 'jasminerice'
  gem 'mocha', require: false
  gem 'rb-fsevent'
  gem 'rb-inotify', '~> 0.8.8', require: RUBY_PLATFORM.include?('linux') && 'rb-inotify'
  gem 'rspec-rails'
  gem 'shoulda'
  gem 'simplecov', require: false
  gem 'terminal-notifier-guard', require: RUBY_PLATFORM.include?('darwin') && 'terminal-notifier-guard'
end

group :development do 
  gem 'better_errors'
  gem 'binding_of_caller'
  gem 'librarian', '>= 0.0.25', require: false
  gem 'pry-rails'
  gem 'awesome_print'
end

# this is an optional gem, it provides a high performance replacement
# to String#blank? a method that is called quite frequently in current
# ActiveRecord, this may change in the future
gem 'fast_blank', github: "SamSaffron/fast_blank"

# IMPORTANT: mini profiler monkey patches, so it better be required last
#  If you want to amend mini profiler to do the monkey patches in the railstie
#  we are open to it.
gem 'rack-mini-profiler', git: 'git://github.com/SamSaffron/MiniProfiler'

# perftools only works on 1.9 atm
group :profile do
  # travis refuses to install this, instead of fuffing, just avoid it for now
  #
  # if you need to profile, uncomment out this line
  # gem 'rack-perftools_profiler', require: 'rack/perftools_profiler', platform: :mri_19 
end
