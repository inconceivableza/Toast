# Toast

This is a theme for [Ghost](http://github.com/tryghost/ghost/). It's based on the default [Source theme](https://github.com/TryGhost/Source/), with some changes, listed in the first section *Changes*.
Some of these have been taken from the [fount](https://github.com/davidfraser/fount/) theme.

# Changes

The following changes have been made from the [Source theme](https://github.com/TryGhost/Source/):

## Technical

* Browser Javascript plugins are loaded through yarn, and packaged automatically.
  This should make adding new dependencies and keeping them up to date easier...

## Styling

* *Tag Styling*: tags are styled with a light instead of font, in lowercase. All tags are shown on posts, not just the primary tag.
* *Menu Styling*: menus are adjusted to handle more and wider items
* *Copyright Notice*: rather than saying "Powered by Ghost", a customizable copyright text appears.

## Bug Fixes

* *Pagination fix*: a [fix to a strange pagination bug in Source](https://github.com/TryGhost/Source/pull/72).

# Source (original theme)

_Information from here on is unaltered from the original [Source README](https://github.com/TryGhost/Source/blob/main/README.md)._

The default theme for [Ghost](http://github.com/tryghost/ghost/). This is the latest development version of Source! If you're just looking to download the latest release, head over to the [releases](https://github.com/TryGhost/Source/releases) page.

&nbsp;

# First time using a Ghost theme?

Ghost uses a simple templating language called [Handlebars](http://handlebarsjs.com/) for its themes.

This theme has lots of code comments to help explain what's going on just by reading the code. Once you feel comfortable with how everything works, we also have full [theme API documentation](https://ghost.org/docs/themes/) which explains every possible Handlebars helper and template.

**The main files are:**

- `default.hbs` - The parent template file, which includes your global header/footer
- `home.hbs` - The homepage
- `index.hbs` - The main template to generate a list of posts
- `post.hbs` - The template used to render individual posts
- `page.hbs` - Used for individual pages
- `tag.hbs` - Used for tag archives, eg. "all posts tagged with `news`"
- `author.hbs` - Used for author archives, eg. "all posts written by Jamie"

One neat trick is that you can also create custom one-off templates by adding the slug of a page to a template file. For example:

- `page-about.hbs` - Custom template for an `/about/` page
- `tag-news.hbs` - Custom template for `/tag/news/` archive
- `author-ali.hbs` - Custom template for `/author/ali/` archive


# Development

Source styles are compiled using Gulp/PostCSS to polyfill future CSS spec. You'll need [Node](https://nodejs.org/), [Yarn](https://yarnpkg.com/) and [Gulp](https://gulpjs.com) installed globally. After that, from the theme's root directory:

```bash
# install dependencies
yarn install

# run development server
yarn dev
```

Now you can edit `/assets/css/` files, which will be compiled to `/assets/built/` automatically.

The `zip` Gulp task packages the theme files into `dist/<theme-name>.zip`, which you can then upload to your site.

```bash
# create .zip file
yarn zip
```

# PostCSS Features Used

- Autoprefixer - Don't worry about writing browser prefixes of any kind, it's all done automatically with support for the latest 2 major versions of every browser.


# SVG Icons

Source uses inline SVG icons, included via Handlebars partials. You can find all icons inside `/partials/icons`. To use an icon just include the name of the relevant file, eg. To include the SVG icon in `/partials/icons/rss.hbs` - use `{{> "icons/rss"}}`.

You can add your own SVG icons in the same manner.


# Copyright & License

Copyright (c) 2013-2025 Ghost Foundation - Released under the [MIT license](LICENSE).
