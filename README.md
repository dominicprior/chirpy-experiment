# My attempt at using Chirpy

I followed "Option 1. Using the Starter" from https://chirpy.cotes.page/posts/getting-started/

Then, going slightly off piste, I am going to try "Setting up Natively (Recommended for Unix-like OS)" via the Windows WSL Ubuntu.

An Ubuntu-24.04 WSL shell says I have jekyll 4.4.1, but when I run "jekyll -v" in this folder, I get:

/home/dominic/gems/gems/bundler-4.0.4/lib/bundler/resolver.rb:356:in `raise_not_found!': Could not find gem 'jekyll-theme-chirpy (~> 7.5)' in locally installed gems. (Bundler::GemNotFound)

Aha!  I am trying "bundle install", which seems to do something.  "jekyll -v" still fails, but "bundle exec jekyll -v" is fine.

This works too: "bundle exec jekyll serve".

I changed the _config.yml baseurl to "/chirpy-experiment"

I ran "bundle lock --add-platform x86_64-linux", and it said

```
Writing lockfile to /mnt/c/git/chirpy-experiment/Gemfile.lock
Fetching gem metadata from https://rubygems.org/.........
Resolving dependencies...
```

but didn't seem to edit Gemfile.lock (maybe because we are running Linux via WSL)

# Chirpy Starter

[![Gem Version](https://img.shields.io/gem/v/jekyll-theme-chirpy)][gem]&nbsp;
[![GitHub license](https://img.shields.io/github/license/cotes2020/chirpy-starter.svg?color=blue)][mit]

A minimal, ready-to-use template for creating a blog with the [**Chirpy**][chirpy] Jekyll theme. Get up and running in minutes with all critical files pre-configured.

## Why This Starter Exists

When installing Chirpy through [RubyGems.org][gem], Jekyll can only read a subset of theme files (`_data`, `_layouts`, `_includes`, `_sass`, `assets`) and limited `_config.yml` options from the gem. As a result, users cannot enjoy the full out-of-the-box experience that Chirpy offers.

To unlock all features, the following files must be present in your Jekyll site:

```shell
.
├── _config.yml
├── _plugins
├── _tabs
└── index.html
```

This starter bundles those files from the latest **Chirpy** release along with a [CD][CD] workflow, so you can start writing immediately.

## Usage

Check out the [theme's docs](https://github.com/cotes2020/jekyll-theme-chirpy/wiki).

## Contributing

This repository is automatically updated with new releases from the theme repository. If you encounter any issues or want to contribute to its improvement, please visit the [theme repository][chirpy] to provide feedback.

## License

This work is published under [MIT][mit] License.

[gem]: https://rubygems.org/gems/jekyll-theme-chirpy
[chirpy]: https://github.com/cotes2020/jekyll-theme-chirpy/
[CD]: https://en.wikipedia.org/wiki/Continuous_deployment
[mit]: https://github.com/cotes2020/chirpy-starter/blob/master/LICENSE
