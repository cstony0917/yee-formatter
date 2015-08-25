Yee RSpec Formatter [![Build Status](https://secure.travis-ci.org/mattsears/nyan-cat-formatter.png)](http://travis-ci.org/mattsears/nyan-cat-formatter)
========

![NYAN](nyan_example.gif)

This is my take on the Yee RSpec Formatter. It simply creates a rainbow trail of test results. It also counts the number of examples as they execute and highlights failed and pending specs.

The rainbow changes colors as it runs. See it in action [here](http://vimeo.com/32424001).

Works with RSpec 1.3, 2 and 3.

Using  Yee
---------------

You can either specify the formatting when using the `rspec` command:

    rspec --format NyanCatFormatter

Or add `--format NyanCatFormatter` to a `.rspec` file placed in your project's root directory,
so that you won't have to specify the `--format` option everytime you run the command.

###Using with Bundler

To use Yee with a project that uses Bundler (Rails or Sinatra f.e.) you need to add Yee dependecy to your Gemfile:

```ruby
group :test do
  gem "nyan-cat-formatter"
end
```

And then run `bundle install`.

Installing it
-------------

```
$ gem install nyan-cat-formatter
```

If you want to use Yee as your default formatter, simply put the options in your .rspec file:

```
--format NyanCatFormatter
```

Playing the Yee song
-------------------------

You can then enjoy playback in two ways:

**1. Play the song only when desired using a command line option:**

Use the following command to run your specs:

```
$ rspec spec -f NyanCatMusicFormatter
```

And enjoy the site of Yee running across your terminal to the Yee song!

**2. Play the song by default when you run your specs:**

Make sure your .rspec file in your application's root directory contains the following:

```
--color
--format NyanCatMusicFormatter
```

Then run `rspec spec` and enjoy Yee formatted text output accompanied by the Yee song by default!

**This currently only works on Mac OS X or on Linux (if you have mpg321 or mpg123 installed).**

Using the Yee Wide Formatter
---------------------------------

The classic Yee Formatter uses a terminal column per test. One
test, and single step that the cat goes ahead. The **Yee Wide
Formatter**, instead, uses the whole terminal width, so the cat will
always end up reaching the end of the terminal.

Simple use it by configuring it as the RSpec formatter:

```
--format NyanCatWideFormatter
```

Contributing
----------

Once you've made your great commits:

1. Fork Yee
2. Create a topic branch - git checkout -b my_branch
3. Push to your branch - git push origin my_branch
4. Create a Pull Request from your branch
5. That's it!

Author
----------
[Matt Sears](http://www.mattsears.com) :: @mattsears
