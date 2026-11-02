source "https://rubygems.org"

ruby file: ".ruby-version"

# Build locally with:
#
#     bundle exec jekyll serve
#
# The site is built and deployed to GitHub Pages by
# .github/workflows/pages.yml on every push to master.
gem "jekyll", "~> 4.4"

# Theme. Stay on minima 2.5.x: the custom layouts (start, tiles, synth,
# fullwidth, category) and the footer override rely on its includes.
gem "minima", "~> 2.5"

group :jekyll_plugins do
  gem "jekyll-formspree"
end

# Local development server (`jekyll serve`), no longer bundled with Ruby 3+.
gem "webrick", "~> 1.9"
