# UCSB's Game Development Club Website

This contains the source content for UCSB's Game Development Club website. We
use [Hugo](https://gohugo.io) as a static site generator.

## Getting Started

Make sure you have `hugo` and `git` installed. Once you have them both
installed, open a terminal (`cmd` on Windows) and run

```plain
git clone https://github.com/ucsb-game-dev-club/ucsb-game-dev-club.github.io.git
cd ucsb-game-dev-club.github.io
```

to copy the website. Retrieve the latest changes with

```plain
git pull
```

Then you can run a local version of the website with

```plain
hugo serve -D
```

which can navigate to by entering `http://localhost:1313` in your web browser.
It will update as you edit the content on the website.

## Editing Content

Most of the pages can be found in the `content` folder. For example,

* `content/about.md`
* `content/resources.md`

### News Posts

To create a news post, run

```plain
hugo new news/<year>/<title>.md
```

where `<year>` is the current year and `<title>` is the title of your post. If
you don't have `hugo` installed, you can copy `archetypes/news.md` to the
`content/news/<year>/<title>` and edit your copy instead. The new post will
automatically be listed in the news listing.

The file for the text above the news listing is located in
`content/news/_index.md`.

### Front Page

The front page file is located in `themes/ucsb-gamedev/layouts/index.html`.

### Page Template

The website page template is located in
`themes/ucsb-gamedev/layouts/_default/baseof.html`. Be careful when editing this
file because you may break something!

## Publishing

Once you are satisfied with your changes and would like to publish a live
version, run the `publish.sh` script. **Warning:** it will automatically build,
commit, and push the site to `master` branch!
