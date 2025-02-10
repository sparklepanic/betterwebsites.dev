---
title: "BetterWebsites Theme Features"
date: "2025-01-12"
draft: "False"
thumbnail: "/webp/lorenzo-herrera-p0j-mE6mGo4-unsplash.webp"
summary: "Just a **test** description**"
tags: 
- web
- blog
---

{{< figure src="/webp/lorenzo-herrera-p0j-mE6mGo4-unsplash.webp" link="/highres/lorenzo-herrera-p0j-mE6mGo4-unsplash.jpg" alt="An arched bridge over a pond of water with greenery all around" caption="*photo by [@lorenzoherrera](https://unsplash.com/photos/vintage-gray-game-console-and-joystick-p0j-mE6mGo4) on Unsplash* | Licensed under [Unsplash License](https://unsplash.com/license)." >}}

This is a simple [gohugo](https://gohugo.io/) theme.
It doesn't use a CSS framework but a smallish custom CSS file, uses a [system font stack](https://systemfontstack.com/) (and also defaults to load [Atkinson Hyperlegible](https://www.brailleinstitute.org/freefont/) if the user has it installed on their system), contains no Javascript, utilizes [bootstrap icons](https://icons.getbootstrap.com/) through SVG, respects dark vs light mode of the user, loads fast, and follows a minimalist/utilitarian/brutalist design. 
All while looking great and being responsive, supporting modern browsers. 
Importantly, it tries to follow a [designed-to-last](https://jeffhuang.com/designed_to_last/) mentality.

## How to add this theme to your GoHugo Site

1. `cd` into your hugo site.
2. Add `git submodule add git@github.com:sparklepanic/betterwebsites.dev.git themes/betterwebsites`
3. `cd` into the theme and fill out the config.toml and you'll be good to go!

### How to update the theme after new updates have been published to Github

1. `cd` into your hugo site
2. `git submodule update --remote`

### If you're downloading your repos with this submodule already in it you'll probably need to:

`git submodule update --init --recursive`


## The homepage is controlled by the main Hugo config

Contents of `hugo.toml` at our site root:

```toml

baseURL = 'https://example.org/'
languageCode = 'en-us'
title = 'betterwebsites.dev'
theme = '../..'
copyright = "Except where otherwise noted, content on this site is licensed under a [Creative Commons Attribution license](https://creativecommons.org/licenses/by/4.0/). Site theme [under MIT license](/theme/LICENSE). This creator is dedicated to the sharing of art, science, and ideas. See the [privacy policy and legal information](/legal) here."
date_format = "2006-01-02" # Because anything other than ISO8601 is folly

[markup.highlight]
style = "dracula"

# This theme is meant to get most of the homepage data right from the config.toml. The `name` parameter will be the title of the homepage, with provided pronouns below the name. The `bio` parameter is piped to Markdownify so you can write your bio in markdown.

[Params]
  name = "BetterWebsites"
  firstname = "BetterWebsites"
  pronouns = "she/they/he/xe"
  bio = """
An example site for this minimalist [GoHugo](https://gohugo.io/) theme so you too can escape the hell that is social media. Bring back the [Myspace era](https://www.codecademy.com/resources/blog/myspace-and-the-coding-legacy/), insightful [blogs](https://manuelmoreale.com/on-the-state-of-the-web), great [info sites](https://transfemscience.org/articles/transfem-intro/), easily readable [RSS](https://www.404media.co/404-media-now-has-a-full-text-rss-feed/), and [a place for all of us on the web](https://indieweb.org/).
  	"""
  
# This is an optional About section. Comment out all the lines from about to the last 3 quote marks to disable.
 
 about = """
- Optional About section. Comment out all the lines from about to the last 3 quote marks to disable in the `hugo.toml`. 
- It's piped to Markdown and accepts shortcodes.

{{</* figure src="/webp/lorenzo-herrera-p0j-mE6mGo4-unsplash.webp" link="/highres/lorenzo-herrera-p0j-mE6mGo4-unsplash.jpg" alt="An arched bridge over a pond of water with greenery all around" caption="*photo by [@lorenzoherrera](https://unsplash.com/photos/vintage-gray-game-console-and-joystick-p0j-mE6mGo4) on Unsplash* | Licensed under [Unsplash License](https://unsplash.com/license)." */>}}
	"""

# Below you can put links for your home page with supported Bootstrap icons

  
 [[Params.links]]
  url = "https://github.com/sparklepanic/betterwebsites.dev"
  text = "BetterWebsites code"
  icon = "github"
  
   [[Params.links]]
  url = "/posts/theme"
  text = "Theme Features"
  icon = "star"


[[Params.links]]
  url = "https://infosec.exchange/"
  text = "Mastodon"
  icon = "mastodon"
  #html_attributes = "rel=\"me\"" # To provide Mastodon verification

[[Params.links]]
  url = "https://instagram.com/"
  text = "Instagram"
  icon = "instagram"

[[Params.links]]
  url = "/posts/index.xml"
  text = "Subscribe via RSS"
  icon = "rss-fill"

  [outputs]
  home = ['html']
  section = ['html', 'rss']
  taxonomy = ['html']
  term = ['html', 'rss']
```

## Examples (this is a Level 2 header)

- Here is *emphasis*
- Here is **bold**
- Here is ~~cross out~~

Here's a table. 
It's just a sample of what a table looks like in this theme.

| Website      | Why it's important | 
| ----------- | ----------- |
| https://en.wikipedia.org      | It has most of human knowledge in a readable, [reliable](https://en.wikipedia.org/wiki/Reliability_of_Wikipedia) format. One of the coolest things to ever exist! |
| https://web.archive.org | The Internet is forever. |
|https://genderdysphoria.fyi/ | "The purpose of this site is to document the many ways that Gender Dysphoria can manifest, as well as the numerous forms of gender transition, in order to provide a guide for those who are questioning, those who are starting their transgender journey, those already on their path, and those who simply wish to be better allies." |
| https://theguardian.com/us | Probably the best current news source out there. |
| https://pmc19.com/data | Best site for current COVID data. |

We can talk about code by talking about things like the `sudo` command with single backticks inline (or as an alternative to kbd like `control` + `alt` + `delete`), or we could do code blocks:

```bash
mkdir example-folder
cd example-folder
touch newfile.md
cat this is some text >> newfile.md
```
Here is [what a link looks like](https://www.youtube.com/watch?v=N9w1lCZfaWI) and here is a block quote:

> It is always brave to insist on undergoing transformations that feel necessary and right even when there are so many obstructions to doing so, including people and institutions who seek to pathologize or criminalize such important acts of self-definition. I know that for some it feels less brave than necessary, but we all have to defend those necessities that allow us to live and breathe in the way that feels right to us. Surgical intervention can be precisely what a trans person needs–it is also not always what a trans person needs. Either way, one should be free to determine the course of one’s gendered life.

--- Judith Butler

Both light-mode and dark-mode styling allows for `a:visited` but with different styling.

{{< box title="Info box example" src="Info boxes with a dedicated custom `shortcode` are supported. You can input a custom title at the top and then this text. It also pipes to `markdownify`. The gradient colors are different between dark and light modes. =)" >}}

This is done by:

```go
{{</* box title="Info box example" src="Info boxes with a dedicated custom `shortcode` are supported. You can input a custom title at the top and then this text. It also pipes to `markdownify`. The gradient colors are different between dark and light modes. =)" */>}}
```

### Level 3 headings are the lowest heading 

The idea is to minimize level 3 headings all-together and just use level 1 and level 2 headings. I'm following Edward Tufte and Richard Feynman's example:

> [It is] notable that the Feynman lectures (3 volumes) write about all of physics in 1800 pages, using only 2 levels of hierarchical headings: chapters and A-level heads in the text. It also uses the methodology of sentences which then cumulate sequentially into paragraphs, rather than the grunts of bullet points. Undergraduate Caltech physics is very complicated material, but it didn’t require an elaborate hierarchy to organize.

--- Edward Tufte, forum post, ‘Book design: advice and examples’ thread

## Media

Images are always hard to get right. Too many images or images that aren't optimized correctly or not displaying alt-text can take away from a good browsing experience.[^1] Same with images not displaying well on different viewports.

The below photo is displayed with [the Hugo *figure* shortcode](https://gohugo.io/content-management/shortcodes/) as such:

```go
{{</* figure src="/webp/soheb-zaidi-AYS2sSAMyhc-unsplash.webp" link="/highres/soheb-zaidi-AYS2sSAMyhc-unsplash.jpg" alt="" caption="*Photo by [@msohebzaidi](https://unsplash.com/photos/people-walking-on-street-during-night-time-AYS2sSAMyhc) on Unsplash* | Licensed under [Unsplash License](https://unsplash.com/license)." */>}}
```

{{< figure src="/webp/soheb-zaidi-AYS2sSAMyhc-unsplash.webp" link="/highres/soheb-zaidi-AYS2sSAMyhc-unsplash.jpg" alt="" caption="*Photo by [@msohebzaidi](https://unsplash.com/photos/people-walking-on-street-during-night-time-AYS2sSAMyhc) on Unsplash* | Licensed under [Unsplash License](https://unsplash.com/license)." >}}

Note that the `src` is to a webp in its own directory and it links to a highres version also in its own directory. The process for this is to:

1. Take the edited jpg and use https://squoosh.app to output a webp photo at a reasonable pixel size
2. Place the squooshed webp into the `webp` directory and the original jpg into the `highres` directory
3. Create the shortcode for the photo in the markdown document
4. Enter the alt-text and caption with optional EXIF

The reason for this process is that I want the website to load fast and the images to not be unwieldy but to allow for people to see or download the full-res images if they'd like to. I also often lazy load images not in the immediate viewport with `loading="lazy"` in the `figure` shortcode.

It also allows me to link the full-res version and send it to people directly if they ask me to SMS it to them or email it to them. I'm not super interested in a traditional gallery style page.

Video is similarly using a shortcode:

```go
{{</* video src="/video/*" autoplay="true" muted="true" loop="true" */>}}
```

{{< video src="/video/5820799-hd_1080_1920_30fps.mp4" autoplay="true" muted="true" loop="true" >}}

Video by [@maksgelatin](https://www.pexels.com/video/hello-there-purple-neo-sign-5820799/) on Pexels. Used under [Pexels license](https://www.pexels.com/license/).

Use the shortcode for Bootstrap Icons to display them: 

```go
{{</* svg ico="lock" */>}} Locked!
```


{{< svg ico="lock" >}} Locked

Or custom SVG's like this one with the svg-plain shortcode: 

```go
{{</* svg-plain "/static/svg/line-md--compass-loop.svg" */>}}
```

{{< svg-plain "/static/svg/line-md--compass-loop.svg" >}}

[Check out all these other cool SVGs at Iconify](https://icon-sets.iconify.design/line-md/). Icon under [MIT license](https://github.com/cyberalien/line-md/blob/master/license.txt)

## Other aspects

This theme has a few other aspects that are worth highlighting:

- When a post has `lastmod` in the frontmatter, it is listed in the blog order with the lastmod date. This will allow modified posts to show up near the top of the blogroll when edited.
- The date format is the year in [ISO8601](https://xkcd.com/1179/)
- Sticky top bar for navigation
- Easily plug in the homepage links to the `config.toml` with Bootstrap icons
- RSS link because [RSS is fucking cool!](https://www.404media.co/404-media-now-has-a-full-text-rss-feed/)
- When selecting text, the text is yellow (except on Apple systems for some reason)
- There is a [custom 404 page](/404)

## Things I plan to add

- An audio short-code for hosted audio
- Add favicon
- Fix descriptions of pages to display relevant metadata when people share links


[^1]: This is what a footnote looks like. I spent hours trying to get `scroll-margin-top` working with the sticky header!!


