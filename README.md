# cf_ruby

Welcome to your new gem! In this directory, you'll find the files you need to be able to package up your Ruby library into a gem. Put your Ruby code in the file `lib/cf/ruby`. To experiment with that code, run `bin/console` for an interactive prompt.

TODO: Delete this and the text above, and describe your gem
See Google blog and documentation:
1) https://cloud.google.com/blog/products/application-development/ruby-comes-to-cloud-functions
2) https://cloud.google.com/functions/docs/console-quickstart
3) https://googlecloudplatform.github.io/functions-framework-ruby/v1.2.0/file.overview.html
4) https://github.com/GoogleCloudPlatform/functions-framework-ruby
5) https://github.com/googleapis/google-cloudevents-ruby

## Installation

Install the gem and add to the application's Gemfile by executing:

    $ bundle add cf-ruby

If bundler is not being used to manage dependencies, install the gem by executing:

    $ gem install cf-ruby

## Usage

TODO: Write usage instructions here

## Development

After checking out the repo, run `bin/setup` to install dependencies. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and the created tag, and push the `.gem` file to [rubygems.org](https://rubygems.org).

bundle install
# ...installs the functions_framework gem and other dependencies
bundle exec functions-framework-ruby --target hello
# ...starts the web server in the foreground

curl http://localhost:8080

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/cf-ruby.
