This is the betterwebsites theme. This is a simple gohugo theme that I’ve been wanting to develop for some time. It doesn’t use a CSS framework but a smallish custom CSS file, uses a system font stack (and also defaults to load Atkinson Hyperlegible if the user has it installed on their system), contains no Javascript, utilizes bootstrap icons through SVG, respects dark vs light mode of the user, loads fast, and follows a minimalist/utilitarian/brutalist design. All while looking great and being responsive, supporting modern browsers. Importantly, it tries to follow a designed-to-last mentality. -Raven Winters

# How to add this to your GoHugo Site

1. `cd` into your hugo site.
2. Add `git submodule add git@github.com:sparklepanic/betterwebsites.dev.git themes/betterwebsites`
3. `cd` into the theme and fill out the config.toml and you'll be good to go!

# How to update the theme after new updates have been published to Github

1. `cd` int your hugo site
2. `git submodule update --remote`

## If you're downloading your repos with this submodule already in it,

`git submodule update --init --recursive`

