# lobber

* What is it?
* What's a gem?
* Anatomy of a gem?
* A quick GitHub tour
* Rspec demo
* Live demo
* Rake tasks
* We'll release the Gem and publish to Ruby gems
* Code tour if there's time

# What is it? What's it do?

Quickly upload a directory to Amazon S3 via a command

# What's a Ruby gem?

A standard package format for distributing Ruby programs and libraries.

# What's Amazon S3?

* [Amazon Simple Storage Service](http://aws.amazon.com/documentation/s3/)
* simple & generally free HTTP server
* highly scalable & convenient

# Why do I care?

* Fast commandline-triggered cloud backup of anything on your computer
* Rapidly publish web applications, prototypes, demos, etc.
* Good example of a Ruby gem

# Getting started with Ruby gems

Bundler has a built-in scaffolding generator:

bundle gem your_gem

# This results in:

```
├── Gemfile
├── LICENSE.txt
├── README.md
├── Rakefile
├── fake_gem.gemspec
└── lib
    ├── fake_gem
    │   └── version.rb
    └── fake_gem.rb
```

# Let's take a look at fake_gem.gemspec:

```Ruby
lib = File.expand_path('../lib', __FILE__)
$LOAD_PATH.unshift(lib) unless $LOAD_PATH.include?(lib)
require 'fake_gem/version'

Gem::Specification.new do |spec|
  spec.name          = "fake_gem"
  spec.version       = FakeGem::VERSION
  spec.authors       = ["Mike Ball"]
  spec.email         = ["mikedball@gmail.com"]
  spec.description   = %q{TODO: Write a gem description}
  spec.summary       = %q{TODO: Write a gem summary}
  spec.homepage      = ""
  spec.license       = "MIT"

  spec.files         = `git ls-files`.split($/)
  spec.executables   = spec.files.grep(%r{^bin/}) { |f| File.basename(f) }
  spec.test_files    = spec.files.grep(%r{^(test|spec|features)/})
  spec.require_paths = ["lib"]

  spec.add_development_dependency "bundler", "~> 1.3"
  spec.add_development_dependency "rake"
end
```

# Back to lobber

Where can I see it?

https://github.com/mdb/lobber

# Features of Note

* using Rspec for unit tests; these are housed in the specs directory
* using [Travis CI](https://travis-ci.org/) for continuous integration
* using [simplecov](https://github.com/colszowka/simplecov) for code coverage analysis
* The 'bin' directory houses executables

# How to run the tests

rake spec

# Coverage

open coverage/index.html

# Live demo

Let's do this!

git clone https://github.com/mdb/lobber.git
cd lobber
rake install
lob coverage

# Release to Ruby gems

* View Rake options: `rake -T`
* Tag, push the tag to Github, and publish this puppy to Rubygems: `rake release`

# Learn more

* [GitHub](http://github.com)
* [Rubygems](http://rubygems.org)
* [Philly.rb](http://phillyrb.org)

# Thanks!

That's it. Questions?
