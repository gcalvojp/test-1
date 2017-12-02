# README

[Lorem ipsum dolor](foo.md) sit amet, consectetur adipiscing elit. Pellentesque et arcu auctor, vulputate sem vel, pellentesque sapien. Vivamus ex dui, pulvinar egestas metus vitae, tincidunt eleifend felis. Maecenas non arcu lacinia, tincidunt sapien et, malesuada orci. Quisque id lorem vitae mi commodo vulputate. Suspendisse varius vitae nibh cursus scelerisque. Aliquam id ex rhoncus, accumsan orci vitae, tincidunt dolor. Etiam molestie lectus tortor, eu mattis mauris sagittis vitae. Aenean sit amet nibh dolor. Phasellus et nibh in tortor consequat vestibulum ac non risus. Nullam luctus suscipit lorem, quis rutrum massa mollis a. Vivamus consequat sem risus, non porta justo feugiat nec. Suspendisse potenti. Nullam dapibus turpis libero, sit amet elementum nibh fermentum a. Cras at varius ligula. In hac habitasse platea dictumst. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.

<textarea>
{{ site | jsonify }}
</textarea>

## Posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>


## Pages

<ul>
  {% for page in site.pages %}
    <li>
      <a href="{{ page.url }}">{{ page.title }}</a>
      {{ page.excerpt }}
    </li>
  {% endfor %}
</ul>


# The Cayman theme

*Cayman is a Jekyll theme for GitHub Pages. You can [preview the theme to see what it looks like](http://pages-themes.github.io/cayman), or even [use it today](#usage).*

![Thumbnail of cayman](thumbnail.png)

## Usage

To use the Cayman theme:

1. Add the following to your site's `_config.yml`:

    ```yml
    theme: jekyll-theme-cayman
    ```

2. Optionally, if you'd like to preview your site on your computer, add the following to your site's `Gemfile`:

    ```ruby
    gem "github-pages", group: :jekyll_plugins
    ```



## Customizing

### Configuration variables

Cayman will respect the following variables, if set in your site's `_config.yml`:

```yml
title: [The title of your site]
description: [A short description of your site's purpose]
```

Additionally, you may choose to set the following optional variables:

```yml
show_downloads: ["true" or "false" to indicate whether to provide a download URL]
google_analytics: [Your Google Analytics tracking ID]
```

### Stylesheet

If you'd like to add your own custom styles:

1. Create a file called `/assets/css/style.scss` in your site
2. Add the following content to the top of the file, exactly as shown:
    ```scss
    ---
    ---

    @import "{{ site.theme }}";
    ```
3. Add any custom CSS (or Sass, including imports) you'd like immediately after the `@import` line

### Layouts

If you'd like to change the theme's HTML layout:

1. [Copy the original template](https://github.com/pages-themes/cayman/blob/master/_layouts/default.html) from the theme's repository<br />(*Pro-tip: click "raw" to make copying easier*)
2. Create a file called `/_layouts/default.html` in your site
3. Paste the default layout content copied in the first step
4. Customize the layout as you'd like

### Sass variables

If you'd like to change the theme's [Sass variables](https://github.com/pages-themes/cayman/blob/master/_sass/variables.scss), set new values before the `@import` line in your stylesheet:

```scss
$section-headings-color: #0086b3;

@import "{{ site.theme }}";
```

## Roadmap

See the [open issues](https://github.com/pages-themes/cayman/issues) for a list of proposed features (and known issues).

## Project philosophy

The Cayman theme is intended to make it quick and easy for GitHub Pages users to create their first (or 100th) website. The theme should meet the vast majority of users' needs out of the box, erring on the side of simplicity rather than flexibility, and provide users the opportunity to opt-in to additional complexity if they have specific needs or wish to further customize their experience (such as adding custom CSS or modifying the default layout). It should also look great, but that goes without saying.

## Contributing

Interested in contributing to Cayman? We'd love your help. Cayman is an open source project, built one contribution at a time by users like you. See [the CONTRIBUTING file](CONTRIBUTING.md) for instructions on how to contribute.

### Previewing the theme locally

If you'd like to preview the theme locally (for example, in the process of proposing a change):

1. Clone down the theme's repository (`git clone https://github.com/pages-themes/cayman`)
2. `cd` into the theme's directory
3. Run `script/bootstrap` to install the necessary dependencies
4. Run `bundle exec jekyll serve` to start the preview server
5. Visit [`localhost:4000`](http://localhost:4000) in your browser to preview the theme

### Running tests

The theme contains a minimal test suite, to ensure a site with the theme would build successfully. To run the tests, simply run `script/cibuild`. You'll need to run `script/bootstrap` one before the test script will work.
