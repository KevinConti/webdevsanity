
# Useful commands for build, deploy, etc

`hugo new site sitename`
Creates a new site. Probably don't need to do this again, but here for reference.

`hugo server --gc --minify -D`
Starts a server for local development, with similar compression / cache clearing as we will run in render

`hugo --gc --minify`
The command to put into render in order to build production assets
