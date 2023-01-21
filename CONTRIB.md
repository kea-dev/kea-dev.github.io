# Contribute
This page is built with Jekyll and hosted using GitHub Pages.

# Posts
You’ll find posts in the `docs/_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the way we revommend is dealing with jekyll - in this repo, a fork of it, or in any other Jekyll site repor is simply:

1. Put your source in a git repo and push it to GitHub
2. On the GitHub web page of your repo ([kea-dev/kea-dev.github.io](https://github.com/kea-dev/kea-dev.github.io - in our case). on the _Code_ tab, hit the green _code_ button and slide over to _CodeSpaces_ and create a new one - the default is all you need.

<img width="407" alt="image" src="https://user-images.githubusercontent.com/155492/213870395-13da006c-d6f6-4015-b703-43fc6d44c3b9.png">

3. Once the new CodeSpace has loaded in your browser, go to the terminal in the bottom and run the following command to prep it for hosting your jelkyll site (note: first time you try to paste someting from the clip board into the CodeSpace, you must allow your browser to do so):
```shell
cd docs
bundler update
bundler install
```
4. To build, serve and automatically watch for file changes and rebuild instantly run the following command (for both this and the previous command, your working directory must be the one where your gemfile sits so you might need to `cd docs`):
```shell
bundler exec jekyll serve
```
5. Jekyll will build and serve the site on the CodeSpace's port 4000. The CodeSpace will automatically detect the started service and offer you a link to visit the outside of the CodeSpace coming in on port 4000 - accept the link and go see your site live - every time you change something in MarkDown files it comes online instantly. If you loose the link - like if you close the browser og tab - you can look it up on the _PORTS_ tab in the bottom panel in the CodeSpace.

**NOTE on `_config.yml`**: The `_config.yml` file constitutes an exception. It is only read during the build process - not the outomated rebuild. So if you want to see changes done in `_config.yml`, you must stop (`CTRL+C`) and restart your service in the terminal.

**NOTE on the terminal**: Your terminal is "occupied" for hosting the Jekyll server, but if you need another to work with your CLI tools in the CodeSpace you can start a new one - as may as you want actually.


# Posts and Frontmatter
Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.md`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `md` is the file extension representing the format used in the file. After that, include the necessary [front matter](https://jekyllrb.com/docs/front-matter/) - which may differ for different layouts. 

Check out the [Jekyll docs](https://jekyllrb.com/docs/home) for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo](https://github.com/jekyll/jekyll). If you have questions, you can ask them on [Jekyll Talk](https://talk.jekyllrb.com/).

