# Solidus User Roles

[![CircleCI](https://circleci.com/gh/solidusio-contrib/solidus_user_roles.svg?style=shield)](https://circleci.com/gh/solidusio-contrib/solidus_user_roles)
[![codecov](https://codecov.io/gh/solidusio-contrib/solidus_user_roles/branch/master/graph/badge.svg)](https://codecov.io/gh/solidusio-contrib/solidus_user_roles)

<!-- Explain what your extension does. -->

## Installation

Add solidus_user_roles to your Gemfile:

```ruby
gem 'solidus_user_roles', github: 'solidusio-contrb/solidus_user_roles'
```

Bundle your dependencies and run the installation generator:

```shell
bundle
bundle exec rails g solidus_user_roles:install
```

Remember to seed or run:
```shell
rake solidus_user_roles:load_seeds
```

Admin Panel
-----------
An admin is the only user who has the ability to add or remove roles from other users.
![image](https://github.com/cpfergus1/solidus_user_roles/assets/68167430/8109fe7e-d098-42c8-a03a-ad1bec273b8c)
![image](https://github.com/cpfergus1/solidus_user_roles/assets/68167430/311d8e38-e801-401d-9fe8-f232435001ad)
![image](https://github.com/cpfergus1/solidus_user_roles/assets/68167430/6f248635-054c-4adc-9fdf-85108acd06c8)
## Development

### Testing the extension

First bundle your dependencies, then run `bin/rake`. `bin/rake` will default to building the dummy
app if it does not exist, then it will run specs. The dummy app can be regenerated by using
`bin/rake extension:test_app`.

```shell
bin/rake
```

To run [Rubocop](https://github.com/bbatsov/rubocop) static code analysis run

```shell
bundle exec rubocop
```

When testing your application's integration with this extension you may use its factories.
You can load Solidus core factories along with this extension's factories using this statement:

```ruby
SolidusDevSupport::TestingSupport::Factories.load_for(SolidusUserRoles::Engine)
```

### Running the sandbox

To run this extension in a sandboxed Solidus application, you can run `bin/sandbox`. The path for
the sandbox app is `./sandbox` and `bin/rails` will forward any Rails commands to
`sandbox/bin/rails`.

Here's an example:

```
$ bin/rails server
=> Booting Puma
=> Rails 6.0.2.1 application starting in development
* Listening on tcp://127.0.0.1:3000
Use Ctrl-C to stop
```

### Releasing new versions

Please refer to the [dedicated page](https://github.com/solidusio/solidus/wiki/How-to-release-extensions) in the Solidus wiki.


## License
Fork of https://github.com/boomerdigital/solidus_user_roles

Copyright (c) 2023 Allison Reilly, released under the New BSD License.
