source "https://rubygems.org"

# Use a more recent Jekyll version that's compatible with Ruby 3.3.0
gem "jekyll", "~> 4.3.2"
gem "webrick", "~> 1.7"
gem "jekyll-sass-converter", "~> 2.2.0"

# Add standard library gems that will be removed from default gems in Ruby 3.4.0
gem "csv"
gem "base64"
gem "bigdecimal"

# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
  gem "jekyll-sitemap", "~> 1.4.0"
  gem "jekyll-seo-tag", "~> 2.7.1"
end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions of the gem
# do not have a Java counterpart.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby] 