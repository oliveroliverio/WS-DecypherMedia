# [Full stack machine learning](https://www.youtube.com/watch?v=KdUa7QQLpng)
Use this instead of the old one

# Ruby Scraping
## Instructions
1. Make directory and cd into it, make gem file
```
mkdir test_<date>
cd test_<date>
vi Gemfile
```

2. Add these lines

```
ruby '2.6.3'
gem 'nokogiri'
gem 'watir'
gem 'pry'
```

3. Run pry by typing the following in terminal

```
pry
```

4. require watir and nokogiri

```
require "nokogiri"
require "watir"
```

5. load instance of chrome (need to have webdriver installed)

```
browser = Watir::Browser.new(:chrome)
```

## Issues
- MissingSpecError

```
Gem::MissingSpecError: Could not find 'racc' (~> 1.4) among 189 total gem(s)
Checked in 'GEM_PATH=/Users/oliveroliverio/.gem/ruby/2.6.0:/Library/Ruby/Gems/2.6.0:/System/Library/Frameworks/Ruby.framework/Versions/2.6/usr/lib/ruby/gems/2.6.0', execute `gem env` for more information
from /System/Library/Frameworks/Ruby.framework/Versions/2.6/usr/lib/ruby/2.6.0/rubygems/dependency.rb:311:in `to_specs'
Caused by Gem::MissingSpecError: Gem::MissingSpecError
from /System/Library/Frameworks/Ruby.framework/Versions/2.6/usr/lib/ruby/2.6.0/rubygems/dependency.rb:311:in `to_specs'
Caused by LoadError: cannot load such file -- nokogiri
from /System/Library/Frameworks/Ruby.framework/Versions/2.6/usr/lib/ruby/2.6.0/rubygems/core_ext/kernel_require.rb:54:in `require'
```

- install missing gem [(racc)](https://rubygems.org/gems/racc/versions/1.4.14).  Be sure to add to gem file

```
sudo gem install racc -v 1.4.14
```

# ----Below doen't work-----
# [Intro to webscraping and browser automation](/Users/oliveroliverio/Downloads/CS/CS.Decypher.Media/_Intro-to-WS-Automation.mp4)

- Make repo
```
gh repo create <repo-name> --public --clone
```
- cd into it

```
code .
```
- make README.md file

- in directory run make rails project directory

```
rails new test_<date> && cd  test_<date>
```

- go to gemfile and add these lines

```
gem 'pry-rails'
gem 'watir'
```

- run bundle in terminal in directory
```
sudo bundle
```

- download chrome driver and move to bin
- within the test_<date dirctory> run the following

```
sudo rails console
```
- currently running into load errors

```
(base) oliveroliverio@Olivers-MacBook-Air test_20211206 % sudo rails console
/Library/Ruby/Gems/2.6.0/gems/msgpack-1.4.2/lib/msgpack.rb:8:in `require': dlsym(0x7fe265ab4430, Init_msgpack): symbol not found - /Library/Ruby/Gems/2.6.0/gems/msgpack-1.4.2/lib/msgpack/msgpack.bundle (LoadError)
	from /Library/Ruby/Gems/2.6.0/gems/msgpack-1.4.2/lib/msgpack.rb:8:in `<top (required)>'
	from /Library/Ruby/Gems/2.6.0/gems/bootsnap-1.7.5/lib/bootsnap/load_path_cache/store.rb:4:in `require'
	from /Library/Ruby/Gems/2.6.0/gems/bootsnap-1.7.5/lib/bootsnap/load_path_cache/store.rb:4:in `block in <top (required)>'
	from /Library/Ruby/Gems/2.6.0/gems/bootsnap-1.7.5/lib/bootsnap/explicit_require.rb:44:in `rescue in with_gems'
	from /Library/Ruby/Gems/2.6.0/gems/bootsnap-1.7.5/lib/bootsnap/explicit_require.rb:40:in `with_gems'
	from /Library/Ruby/Gems/2.6.0/gems/bootsnap-1.7.5/lib/bootsnap/load_path_cache/store.rb:4:in `<top (required)>'
	from /Library/Ruby/Gems/2.6.0/gems/bootsnap-1.7.5/lib/bootsnap/load_path_cache.rb:61:in `require_relative'
	from /Library/Ruby/Gems/2.6.0/gems/bootsnap-1.7.5/lib/bootsnap/load_path_cache.rb:61:in `<top (required)>'
	from /Library/Ruby/Gems/2.6.0/gems/bootsnap-1.7.5/lib/bootsnap.rb:5:in `require_relative'
	from /Library/Ruby/Gems/2.6.0/gems/bootsnap-1.7.5/lib/bootsnap.rb:5:in `<top (required)>'
	from /Library/Ruby/Gems/2.6.0/gems/bootsnap-1.7.5/lib/bootsnap/setup.rb:2:in `require_relative'
	from /Library/Ruby/Gems/2.6.0/gems/bootsnap-1.7.5/lib/bootsnap/setup.rb:2:in `<top (required)>'
	from /Users/oliveroliverio/Git/WS-DecypherMedia/test_20211206/config/boot.rb:4:in `require'
	from /Users/oliveroliverio/Git/WS-DecypherMedia/test_20211206/config/boot.rb:4:in `<top (required)>'
	from /Users/oliveroliverio/Git/WS-DecypherMedia/test_20211206/config/application.rb:1:in `require_relative'
	from /Users/oliveroliverio/Git/WS-DecypherMedia/test_20211206/config/application.rb:1:in `<top (required)>'
	from /Library/Ruby/Gems/2.6.0/gems/spring-2.1.1/lib/spring/application.rb:92:in `require'
	from /Library/Ruby/Gems/2.6.0/gems/spring-2.1.1/lib/spring/application.rb:92:in `preload'
	from /Library/Ruby/Gems/2.6.0/gems/spring-2.1.1/lib/spring/application.rb:157:in `serve'
	from /Library/Ruby/Gems/2.6.0/gems/spring-2.1.1/lib/spring/application.rb:145:in `block in run'
	from /Library/Ruby/Gems/2.6.0/gems/spring-2.1.1/lib/spring/application.rb:139:in `loop'
	from /Library/Ruby/Gems/2.6.0/gems/spring-2.1.1/lib/spring/application.rb:139:in `run'
	from /Library/Ruby/Gems/2.6.0/gems/spring-2.1.1/lib/spring/application/boot.rb:19:in `<top (required)>'
	from /System/Library/Frameworks/Ruby.framework/Versions/2.6/usr/lib/ruby/2.6.0/rubygems/core_ext/kernel_require.rb:54:in `require'
	from /System/Library/Frameworks/Ruby.framework/Versions/2.6/usr/lib/ruby/2.6.0/rubygems/core_ext/kernel_require.rb:54:in `require'
	from -e:1:in `<main>'
```
- searching [solutions](https://stackoverflow.com/questions/12591585/rails-console-not-loading/39938403)

- will finish this later