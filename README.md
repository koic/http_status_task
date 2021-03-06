# HttpStatusTask

`http_status_task` adds rake tasks which print HTTP status codes defined in Rack.

## Installation

```ruby
gem 'http_status_task'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install http_status_task

## Usage

If you want to use in Rails project
```
$ bundle exec rake -T

rake http:status      # Print HTTP status codes, descriptions and symbols
rake http:status:100  # Print HTTP status codes of 100 - 102
rake http:status:200  # Print HTTP status codes of 200 - 226
rake http:status:300  # Print HTTP status codes of 300 - 308
rake http:status:400  # Print HTTP status codes of 400 - 431
rake http:status:500  # Print HTTP status codes of 500 - 511

$ bundle exec rake http:status:100

code description                     symbol
100  Continue                        :continue
101  Switching Protocols             :switching_protocols
102  Processing                      :processing
```

If you want to use in command line

```
$ http_status
code description                     symbol
100  Continue                        :continue
101  Switching Protocols             :switching_protocols
102  Processing                      :processing
...

$ http_status 200
code description                     symbol
200  OK                              :ok
201  Created                         :created
202  Accepted                        :accepted
203  Non-Authoritative Information   :non_authoritative_information
204  No Content                      :no_content
205  Reset Content                   :reset_content
206  Partial Content                 :partial_content
207  Multi-Status                    :multi_status
208  Already Reported                :already_reported
226  IM Used                         :im_used
```

## Contributing

1. Fork it ( https://github.com/muryoimpl/http_status_task/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
