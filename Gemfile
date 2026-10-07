source "https://rubygems.org"

# Use the github-pages gem so the site builds identically to how GitHub
# Pages will build it. This pins Jekyll + plugins to GitHub's supported set.
gem "github-pages", group: :jekyll_plugins

group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-sitemap"
  gem "jekyll-seo-tag"
end

# Windows/JRuby support, harmless elsewhere
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw]
gem "webrick", "~> 1.8"
