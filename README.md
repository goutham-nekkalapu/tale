# Tale

[![Gem Version](https://badge.fury.io/rb/tale.svg)](https://badge.fury.io/rb/tale)

Tale is a minimal Jekyll theme curated for storytellers. This version of 'tale'theme add a few more features on 
top of base version, checkout the demo [here](https://vipulmahadik.github.io/tale/).

# Contents
- [Features](#Features)
- [Installation](#Installation)
- [Usage](#Usage)
- [Customizations](#Customizations)
- [Contributing](#Contributing)

## Features
- Easy installation
- Compatible with GitHub Pages
- Responsive design (looks just as good on mobile)
- Syntax highlighting, with the help of Pygments
- Markdown and HTML text formatting
- Pagination of posts
- [Disqus comments (can be enabled if needed)](#enabling-comments)

## Installation
There are 3 ways to install this theme

1. Install it as a Ruby Gem (for self-hosted sites)
2. Install it with the `jekyll-remote-theme` plugin (for GitHub Pages hosted sites)
3. Fork the project directly

### Ruby Gem method
1. Add this line to your `Gemfile`:

```ruby
gem "tale"
```

2. Install the theme's gems and dependencies:

```bash
$ bundle
```

3. In `_config.yml` add these lines:

```yaml
theme:      tale

permalink:  /:year-:month-:day/:title
paginate:   5
```

Remove any other `theme:` lines.

4. Rename `index.md` to `index.html`. Without this, the `jekyll-paginate` gem will not work.

5. In `about.md`, change the `layout:` field to `post`:

```Markdown
layout: post
```

### GitHub Pages method
1. Add these 2 lines in to your `Gemfile`:

```ruby
gem "jekyll-remote-theme"
gem "jekyll-paginate"
```

2. Install the newly added gems:

```bash
$ bundle
```

3. In `_config.yml` add these lines:

```yaml
remote_theme: chesterhow/tale

permalink:    /:year-:month-:day/:title
paginate:     5

plugins:
  - jekyll-paginate
  - jekyll-remote-theme
```

Remove any other `theme:` or `remote_theme:` lines.

4. Rename `index.md` to `index.html`. Without this, the `jekyll-paginate` gem will not work.

5. In `about.md`, change the `layout:` field to `post`:

```Markdown
layout: post
```

### Fork method
1. Fork this repository

2. Delete the unnecessary files/folders: `CODE_OF_CONDUCT.md`, `LICENSE`, `README.md`, `tale.gemspec`

3. Delete the `baseurl` line in `_config.yml`:

```yaml
baseurl:  "/tale"   # delete this line
```

## Usage
Once you've installed the theme, you're ready to work on your Jekyll site. To start off, I would recommend updating `_config.yml` with your site's details.

To build and serve your site, run:

```bash
$ bundle exec jekyll serve
```

And you're all set! Head over to http://127.0.0.1:4000/ to see your site in action.

### Enabling Comments
Comments are disabled by default. To enable them, look for the following line in `_config.yml` and change `jekyll-tale` to your site's Disqus id.

```yml
disqus: jekyll-tale
```

Next, add `comments: true` to the YAML front matter of the posts which you would like to enable comments for.

## Customizations

- For adding "GA" tracking refer to this [link](https://desiredpersona.com/google-analytics-jekyll/)
- For adding "Disquss" support refer to this [link](https://desiredpersona.com/disqus-comments-jekyll/)
- For enabling SSL for the blog using github's url or custom domain refer to [this](https://blog.webjeda.com/jekyll-ssl/)
- For adding new tabs to exsting ones like (Home, Blog, etc), follow below steps 
  - add the new tab name's URL in '_includes/navigation.html'; can refer to how others tabs are like 'Home', 'Blog' etc were added
  - Create a markdown file in '_pages' dir by the same name with wich the URL was created in above step
  - Add 'layout' and 'permalink' and other attributes to this markdown file; check other markdowns in '_pages' directory for reference

- For updating/adding new social media links,
  - Edit home.html for adding new profile links like (Quora etc)
  - For adding fonts for the newly added social media profiles, search for a font from websites like [this one](https://fontawesome.com/), copy the html code provided there and add it in home.html page.

- For changing Thumbnail for the site, do the following
  - create/use a favicon from one of the free websites like [this one](https://favicon.io/), download the favicon images generated.
  - place the favicon.ico in main directory but all others in 'assets' directory

  ### Making changes to any UI components
  - Run the Jekyll blog on your local machine, open the blog in chrome, go to the UI component where you want to make a change, right click and select inspect page option. This would open google developer tools console for this page.

  - Once the developer tools are open, play the variables like height, color etc for the UI component upto your satisfaction. Identify the class and file names to which the variables you are playing with belong to.

  - Go to those files and update these class variables with the ones you decided from above step.

## Contributing
Found a bug or have a suggestion? Feel free to create an issue or make a pull request!

