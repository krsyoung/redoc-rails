# ReDoc-Rails

A Ruby Gem wrapper for the ReDoc OpenAPI Specification dynamic documentation
project: https://github.com/Rebilly/ReDoc/.

[![Gem Version](https://badge.fury.io/rb/redoc-rails.svg)](http://badge.fury.io/rb/redoc-rails)

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'redoc-rails'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install redoc-rails

## Usage

Add this line to your application's `assets/javascripts/application.js`:

```ruby
//= require ...
//= require redoc.min
//= require ...
```

Add the following to a web page:
```html
  <redoc></redoc>
```

Add the following to the appropriate js/coffee file:

```
# Turbolinks 5
$(document).on 'turbolinks:load', ->
  Redoc.init('/swagger.yml', {})
  return

# vanilla JS
ready = ->
  Redoc.init('/swagger.yml', {})

$(document).ready(ready)
$(document).on('page:load', ready)
```

If you want detailed information on it usage, you can refer to original documentation.

[https://github.com/Rebilly/ReDoc](https://github.com/Rebilly/ReDoc)

## Changelog

  - v1.19.0: bump, stop shipping the unminified version to save space
  - v1.3.3 : bump
  - v1.3.2 : bump
  - v1.3.0 : initial version

## Contributing

1. Fork it ( https://github.com/[my-github-username]/redoc-rails/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
