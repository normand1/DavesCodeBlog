source "https://rubygems.org"

# Run Jekyll with `bundle exec`, e.g. `bundle exec jekyll serve`.
#
# This site is built and published by GitHub Pages, which uses the
# `github-pages` gem to pin Jekyll + plugins to the exact versions GitHub
# runs server-side. That way, what you see locally matches what goes live.
# To update to the versions GitHub currently uses, run: bundle update github-pages
gem "github-pages", group: :jekyll_plugins

# Plugins. jekyll-feed generates /feed.xml for RSS readers.
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
end

# Ruby 3.0+ no longer ships webrick in the standard library, and
# `jekyll serve` needs it to run the local preview server.
gem "webrick", "~> 1.8"

# Windows and JRuby do not include zoneinfo files, so bundle the tzinfo-data gem.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.1", platforms: [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions
# of the gem do not have a Java counterpart.
gem "http_parser.rb", "~> 0.6.0", platforms: [:jruby]
