+++
screenshot = "/images/hugo-icarus.screenshot.png"
thumbnail = "/images/hugo-icarus.tn.png"
demo = "/theme/hugo-icarus/"
source = "https://github.com/digitalcraftsman/hugo-icarus-theme.git"
name = "Icarus"
license = "MIT"
licenselink = "//github.com/digitalcraftsman/hugo-icarus-theme/blob/master/LICENSE.md"
description = "The blog theme you may fall in love with, coming to Hugo. "
homepage = "//github.com/digitalcraftsman/hugo-icarus-theme"
tags = ["syntax highlighting", "maxthjax", "rss", "gallery", "widgets", "google analytics", "useful shortcodes", "responsive"]
features = ["syntax highlighting", "maxthjax", "rss", "gallery", "widgets", "google analytics", "useful shortcodes", "responsive"]
min_version = 0.14

[author]
  name = "Digitalcraftsman"
  homepage = "//github.com/digitalcraftsman"

# If porting an existing theme
[original]
  name = "Ruipeng Zhang"
  homepage = "//blog.zhangruipeng.me"
  repo = "//github.com/ppoffice/hexo-theme-icarus"

+++

# Icarus

Icarus is a responsive and customizable theme for bloggers. It's a port of the same-named theme for [Hexo](//hexo.io) made by [Ruipeng Zhang](https://github.com/ppoffice). Noteworthy features of this Hugo theme are the integration of a comment-system powered by Disqus, localization (l10n) support, syntax highlighting for source code, optional widgets for the sidebar and a handful [shortcodes](http://gohugo.io/extras/shortcodes/) to make your life easier.

![](https://raw.githubusercontent.com/digitalcraftsman/hugo-icarus-theme/master/images/screenshot.png)

## Get the theme

I assume you've Git installed. Inside the folder of your Hugo site run

    $ mkdir themes
    $ cd themes
    $ git clone git@github.com:digitalcraftsman/hugo-icarus-theme.git

You should see a folder called `hugo-icarus-theme` inside the `themes` directory, that we created a few moments ago. For more information read the official [setup guide](https://gohugo.io/overview/installing/) of Hugo.


## Setup

In the next step navigate to the `exampleSite` folder at `themes/hugo-icarus-theme/exampleSite/`. It's structure shoud look similar to this:

    exampleSite
    ├── config.toml
    ├── content
    │   └── post
    │       ├── creating-a-new-theme.md
    │       ├── go-is-for-lovers.md
    │       ├── hugo-is-for-lovers.md
    │       ├── introducing-icarus-and-its-features.md
    │       ├── linked-post.md
    │       └── migrate-from-jekyll.md
    ├── data
    │   └── l10n.toml
    └── static
        └── banners
            └── placeholder.png

In order to get your site running, you need to copy `config.toml` and `data/l10n.toml` into the root folders.


## The config file

Now, let us take a look into the `config.toml`. Feel free to play around with the settings.


### Comments

The opional comment system is powered by Disqus. Enter your shortname to enable the comment section under your posts.

    disqusShortname = ""


### Menu

You can also define the items menu entries as you like. First, let us link a post that you've written. We can do this in the frontmatter of the post's content file by setting `menu` to `main`.

    +++
    menu = "main"
    +++

Furthermore, we can add entries that don't link to posts. Back in the `config.toml` you'll find a section for the menus:

    [[params.menu]]
        before = true
        label  = "Home"
        link   = "/"

Define a label and enter the URL to resource you want to link. With `before` you can decide wether the link should appear before **or** after all linked posts in the menu. Therefore, `Home` appears before the linked post.


### Tell me who you're

This theme also provides a profile section on the left. Add your social network accounts to the profile section on the left by entering your username under `social`. The links to your account will be create automatically.


### Widgets

Beside the profile section you can add widgets on the right sidebar. The following widgets are available:

- recent articles
- category list
- tag list
- tag cloud

You can deactivate them under `params.widgets`:

    [params.widgets]
        recent_articles = false
        categories = true
        tags = true
        tag_cloud = true




## Localization (l10n)

You don't blog in english and you want to translate the theme into your native locale? No problem. Take a look in the `data` folder and you'll find a file `l10n.toml` that we've copied at the beginning. It contains all strings related to the theme. Just replace the original strings with your own.


## Linking thumbnails

After creating a new post you can define a banner by entering the relative path to the image.

    banner = "banners/placeholder.png"

This way you can store them either next to the content file or in the `static` folder.


## Mathematical equations

In case you need to display equations you can insert your Latex or MathML code and it works out of the box thanks to [MathJax](https://www.mathjax.org).


## Shortcodes

Last but not least I included some useful [shortcodes](http://gohugo.io/extras/shortcodes/) to make your like easier.


### Gallery

This way you can include a gallery into your post. Copy the code below into your content file and enter the relative paths to your images.

    {{< gallery
        "/banners/placeholder.png"
        "/banners/placeholder.png"
        "/banners/placeholder.png"
    >}}


### Github Gists

Enter the id of your gist and you're ready to go.

    {{</*  gist "85f59771b5ae1e2091a8" */>}}

Note, that this only works with public gists since authentification is not supported.

### JSFidde

It works the same with JSFiddle examples you want to showcase. The parameter `id` consists of the username and id of the example.

    {{</* jsfiddle id="zalun/NmudS" */>}}

As descibed in the [docs of JSFiddle](http://doc.jsfiddle.net/use/embedding.html), you can define which tabs will be shown. Enter the tabs you want to see separated by a comma in the `tabs` parameter.

    {{</* jsfiddle id="zalun/NmudS" tabs="html,result" */>}}

### Vimeo and Youtube

The embedding of videos from Vimeo and Youtube is also supported.

    {{</* youtube "w7Ft2ymGmfc" */>}}

    {{</* vimeo "137643804" */>}}


## Nearly finished

In order to see your site in action, run Hugo's built-in local server.

    $ hugo server -w

Now enter [`localhost:1313`](//localhost:1313) in the address bar of your browser.


## Contributing

Did you found a bug or got an idea for a new feature? Feel free to use the [issue tracker](//github.com/digitalcraftsman/hugo-icarus-theme/issues) to let me know. Or make directly a [pull request](//github.com/digitalcraftsman/hugo-icarus-theme/pulls).


## License

This theme is released under the MIT license. For more information read the [license](https://github.com/digitalcraftsman/hugo-icarus-theme/blob/master/LICENSE.md).


## Annotations

Thanks to [Steve Francia](//github.com/spf13) for creating Hugo and the awesome community around the project.
