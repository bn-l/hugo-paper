
## Major changes to base hugo-paper theme

- Fixed display on mobile devices
- Improved templates for taxonomies and terms
- Added a new Archives template
- Completely renovated the default list template (improved logic, organised jumbled pieces into separate partials / templates)
- Added opengraph internal template to head
- Added [mermaid](https://mermaid.js.org/intro/n00b-gettingStarted.html#_1-using-the-live-editor) support (markdown diagrams)
- Main content now wraps on word-break (necessary for mobile view)
- Image render hook: If you have a directory like this:

content/
├── posts/
│   ├── images/
│   ├── post1.md
│   └── post2.md

And you reference an image in a post like this: `images/someimage.jpg`, hugo will not link it correctly. The custom render hook fixes this.


## Options

Available options to `config.toml` or `hugo.toml`:

```toml
disqusShortname = 'YOUR_DISQUS_SHORTNAME'   # use disqus comments

[params]
  # color style
  color = 'linen'                           # linen, wheat, gray, light

  # header social icons
  twitter = 'YOUR_TWITTER_ID'               # twitter.com/YOUR_TWITTER_ID
  github = 'YOUR_GITHUB_ID'                 # github.com/YOUR_GITHUB_ID
  instagram = 'YOUR_INSTAGRAM_ID'           # instagram.com/YOUR_INSTAGRAM_ID
  linkedin = 'YOUR_LINKEDIN_ID'             # linkedin.com/in/YOUR_LINKEDIN_ID
  mastodon = 'YOUR_MASTODON_LINK'           # e.g. 'https://mastodon.instance/@xxx'
  rss = true                                # show rss icon

  # home page profile
  avatar = 'GRAVATAR_EMAIL'                 # gravatar email or image url
  name = 'YOUR_NAME'
  bio = 'YOUR_BIO'


  # misc
  disableHLJS = true                        # disable highlight.js
  disablePostNavigation = true              # disable post navigation
  monoDarkIcon = true                       # show monochrome dark mode icon
  gravatarCdn = 'GRAVATAR_CDN_LINK'         # e.g. 'https://cdn.v2ex.com/gravatar/'
  graphCommentId = "YOUR_GRAPH_COMMENT_ID"  # use graph comment (disqus alternative)
  math = true                               # enable KaTeX math typesetting globally
```

Available options to front matter:

```toml
comments = false                            # disable comments for a specific page
math = true                                 # enable KaTeX math typesetting for a specific page
```

## Install

### As hugo module

Inside the folder of your Hugo project, run:

```bash
hugo mod init github.com/<USERNAME>/<REPONAME>
```

Add paper theme ad dependency of your site:

```bash
hugo mod init github.com/<USERNAME>/<REPONAME>
```

Open `config.toml` or `hugo.toml`, remove the `theme` line (if present) and add module section at the bottom of the file:

```toml
[module]
  [[module.imports]]
    path = "github.com/nanxiaobei/hugo-paper"
```

For more information, please read the [official guide](https://gohugo.io/hugo-modules/use-modules/#use-a-module-for-a-theme) of Hugo.

### As git submodule

Inside the folder of your Hugo project, run:

```bash
git submodule add https://github.com/nanxiaobei/hugo-paper themes/paper
```

Open `config.toml` or `hugo.toml`, change `theme` to `"paper"`:

```toml
theme = "paper"
```

For more information, please read the [official guide](https://gohugo.io/getting-started/quick-start/#configure-the-site) of Hugo.

## License

[MIT License](https://github.com/nanxiaobei/hugo-paper/blob/main/LICENSE) (c) [nanxiaobei](https://lee.so/)
