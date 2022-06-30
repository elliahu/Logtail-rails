# Logtail Rails

Collect logs directly from Ruby on Rails projects.
**Supported language versions:**
Ruby 2.7.0 or newer
Rails 6.1.4.2 or newer

You can learn more about using Logtail in Ruby on Rails projects in our [official docs](https://logtail-main.readme.io/docs/installing-logtail-2).

# Installation and setup

You can install Logtail to your Rails projects using the Ruby Bundler.

### Ruby Bundler

If you have Ruby bundler already installed you can skip this step. Run the following command to install the ruby bundler:

```bash
sudo apt install ruby-bundler
```

## Ruby on Rails

To install Logtail to your Ruby on Rails project, run the following command

```bash
bundle add logtail-rails
```

Alternatively, add `gem "logtail-rails"` to your `Gemfile` manually and then run `bundle install`

Then run the following command to create the default config file:

```bash
bundle exec rake logtail:install source_token=YOUR_LOGTAIL_SOURCE_TOKEN
```

Don’t forget to replace `YOUR_LOGTAIL_SOURCE_TOKEN` with your actual source token which you can find in the source settings. This will generate `config/initializers/logtail.rb`.

# Example project

To help you get started and integrate Logtail in your projects, we have prepared an example Rails project. 

## How to run the example project

First, download or clone the repository into the select directory. Make sure you are in the projects directory and run the following command:

```bash
bundle install
```

This will install all dependencies listed in the `Gemfile.lock` file.

Then run the example project by executing the following command:

```bash
rails server
```

This will open a local server [127.0.0.1:3000](http://127.0.0.1:3000). On the main page, click the "Let's go!" button to generate test logs.

You should see the following output:
```
All done!
Log into your Logtail account to check your logs.
```

This will create a total of 6 different logs, each corresponding to a different log level and one with additional structured data. You can review these logs in Logtail.
