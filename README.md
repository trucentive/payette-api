Payette API Documentation
-------------------------

This repository contains doducmentation for the Payette API. The documentation is based on the [Slate API documention system](https://github.com/slatedocs/slate) which creates API documentaiton from specially formatted Markdown.

Deployed to github pages: https://trucentive.github.io/payette-api/#introduction

Getting Started
------------------------------

### Prerequisites

You're going to need:

 - **Linux or macOS** — Windows may work, but is unsupported.
 - **Ruby, version 3.2.1 or newer**
 - **Bundler** — If Ruby is already installed, but the `bundle` command doesn't work, just run `gem install bundler` in a terminal.

### Getting Set Up

1. Clone this repository
2. Initialize and start Slate. You can either do this locally, or with Vagrant:

```shell
# either run this to run locally
bundle install
bundle exec middleman server

# OR run this to run with vagrant
vagrant up
```

You can now see the docs at http://localhost:4567.

Now that Slate is all set up on your machine, you'll probably want to learn more about [editing Slate markdown](https://github.com/slatedocs/slate/wiki/Markdown-Syntax), or [how to publish your docs](https://github.com/slatedocs/slate/wiki/Deploying-Slate).

If you'd prefer to use Docker, instructions are available [in the wiki](https://github.com/slatedocs/slate/wiki/Docker).

### Editing documentation

The documentation source is contained in the source/ directory and the root is the index.md.erb file. Documentation on [editing Slate markdown](https://github.com/slatedocs/slate/wiki/Markdown-Syntax).

### Publishing documentation

There is a deploy.sh script in the repository that will push the documentation to github in a gh-pages branch for github pages:

```shell
./deploy.sh
```

If you need to build the documentation separately you can do it with this command:

```shell
bundle exec middleman build --clean
```

### Note on JavaScript Runtime

For those who don't have JavaScript runtime or are experiencing JavaScript runtime issues with ExecJS, it is recommended to add the [rubyracer gem](https://github.com/cowboyd/therubyracer) to your gemfile and run `bundle` again.
