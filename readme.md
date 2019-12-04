
# Useful commands for build, deploy, etc

`hugo new site sitename`
Creates a new site. Probably don't need to do this again, but here for reference.

`hugo server --gc --minify -D`
Starts a server for local development, with similar compression / cache clearing as we will run in render

`hugo --gc --minify`
The command to put into render in order to build production assets

# Notes - Personal references just so I don't forget things

The theme by itself modifies the themesDirectory location in the config.toml, so you have to change that before the theme will work at the root

config.toml needs to have the relative root, like so:
`baseurl = "//webdevsanity.onrender.com/"`
Otherwise it doesn't pull the root url

For syntax highlighting, you MUST have the angled bracket touch the curly brace:

``` css
{{< highlight css >}}
  body {
      display: contents;
  }
{{< /highlight >}}
```
