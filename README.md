![Ruby](https://github.com/mauricio-doctible/config-parser//actions/workflows/ruby.yml/badge.svg)

# ConfigParser

This utility package reads a file in a format

```
# This is a comment, ignore it
# All these config lines are valid
host = test.com
server_id=55331
cost=2.56
user= user
# comment can appear here as well
verbose =true
test_mode = on
debug_mode = off
log_file_path = /tmp/logfile.log
send_notifications = yes
```

And returns a hash such as

```
{
  'host' => 'test.com',
  'server_id' => 55331,
  'cost' => 2.56,
  'user' => 'user',
  'verbose' => true,
  'test_mode' => true,
  'debug_mode' => false,
  'log_file_path' => '/tmp/logfile.log',
  'send_notifications' => true
}
```

## Development

This code was designed as a rubygem because the scaffold generates an adequate ruby project structure. Nevertheless, this gem was not and should not be published to https://rubygems.org

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`.

### Usage

After installing dependencies locally, run `exe/config_parser spec/fixtures/original_data.txt` to print the parsed hash.

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/config_parser. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [code of conduct](https://github.com/[USERNAME]/config_parser/blob/master/CODE_OF_CONDUCT.md).

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Code of Conduct

Everyone interacting in the ConfigParser project's codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/mauricio-doctible/config_parser/blob/master/CODE_OF_CONDUCT.md).
