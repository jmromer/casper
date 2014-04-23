Casper (for Octopress)
================

An Octopress port of Ghost's Casper theme, with GitHub-style syntax highlighting (or alternate [Twilight theme](http://gist.github.com/iq9/2906599)).

## Preview

![Blog Index](http://s3.amazonaws.com/gh_pages/casper/screen1.jpg)
![Code Snippet](http://s3.amazonaws.com/gh_pages/casper/screen2.jpg)


## Prerequisites

This theme uses kramdown and coderay for syntax highlighting. Ensure the following changes are made before generating your octopress site.

In `\Gemfile`:

```ruby
group :development do
# .
# .
# .
  gem 'kramdown'
  gem 'coderay'
end
```

In `\_config.yml`:

```yaml
# markdown: rdiscount
# rdiscount:
#   extensions:
#     - autolink
#     - footnotes
#     - smart

markdown: kramdown
kramdown:
  use_coderay: true
  coderay:
    coderay_line_numbers: nil
    coderay_css: class

pygments: false # default python pygments have been replaced by pygments.rb
```


## Installation

### Using `git submodule`

#### Installing
```
$ cd <your octopress directory>
$ git submodule add https://github.com/jmromer/casper.git .themes/casper
$ git submodule update --init
$ rake install['casper']
$ rake generate
```

#### Updating
```
$ cd <your octopress directory>
$ git submodule update
$ rake install['casper']
# regenerate, make changes, etc...
```

### Using `git clone`

#### Installing
```
$ cd <your octopress directory>
$ git clone https://github.com/jmromer/casper .themes/casper
$ rake install['casper']
$ rake generate
```

#### Updating
```
$ cd <your octopress directory>/.themes/casper
$ git pull
$ rake install['casper']
# regenerate, make changes, etc...
```


## Thanks!

Thanks to the following developers for their contributions here:

[Kat Hagan](http://github.com/codebykat)<br>
[Russell Brooks](http://github.com/iq9)<br>
[Alejandra Estanislao](http://github.com/alestanis)<br>
[Rosario Rascuna](http://github.com/rosario)<br>
[Rob Dodson](http://github.com/robdodson)<br>

Pull requests are welcome!

## License

(The MIT License)

Copyright © 2014 Jake Romer

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the ‘Software’), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED ‘AS IS’, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
