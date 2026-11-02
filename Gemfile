source "https://rubygems.org"

ruby file: ".ruby-version"

# Build locally with:
#
#     bundle exec jekyll serve
#
# The site is built and deployed to GitHub Pages by
# .github/workflows/pages.yml on every push to master.
gem "jekyll", "~> 4.4"

# The theme lives in this repository (_layouts, _includes, _sass). It started
# as a copy of minima 2.5.2 (MIT, see _sass/elaoin/LICENSE-minima.txt).
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.18"
  gem "jekyll-seo-tag", "~> 2.9"
  gem "jekyll-formspree", "~> 0.1"
end

# Local development server (`jekyll serve`), no longer bundled with Ruby 3+.
gem "webrick", "~> 1.9"
