# kea-dev.github.io

## Separate _what_ from _how_

This repo is for documentation - it's meant to be a show case of the principle; **"separate _what_ form _how_""**. Where _what_ referes to content and _how_ referes to layout. 

Content are the things you just want to get off you chest - essentially the stuff you would probably put in a `README.md` like this using just the very basic features of `MarkDown` to prettify your messages. And _how_ is then refering to the presentations of that content; The layout, the fonts, the grid, the stylesheets, the mobile-first optimizations, the table of contents, the menu bar, the footer - and all that jazz. Essentially all the stuff you _don't_ get when you are just hacking MarkDown files on GitHub. But which you would _like_ to have -  because your want your content to be presented beautifully - as if it was more than what it is; just MarkDown files.

Hey - we do apprecialt beauty!

## Jekyll and GitHub pages
This page is built with [jekyll](https://github.com/jekyll) and hosted using GitHub Pages. 

Jekyll is a multicompiler - a static web site generator. It's Open Source, [written in Ruby](https://github.com/jekyll/jekyll) - by the folks at GitHub, with the specific purpose of adding pretty layout to simple MarkDown files. Most importantly Jekyll compiles MarkDown and Liquid into HTML and SASS/SCSS in to CSS. But Jekyll is also a toolbox, which provides you easy access to setting up a development environment, adding new content, building your site interactively and showing it realtime in a browser.

Like any tool Jekyll, MarkDown, Liquid, CSS takes a bit of training and the technologies have very different learning curves. MarkDown is considered easy - _very easy_ as a matter of fact. While template languages - such as Liquid are often notoriously harder to learn - and they look ugly - and Liquid is not different. CSS and what ever grid framework you choose to optimize your layout  and make it and mobile-first are probably somewhere there in the middle.

So to paraphrase the goal: 

>_With this site we're trying to create a beautiful website, but still only want the actual MarkDown in the repository - only the the documentation that the developers want to get off their chest - not the layout._

## Out of the box
GitHub Pages want this too - and Jekyll was built for this purpose. So out-of-the-box GitHub Pages offers a [special case for Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll); you get an automated build process - like an implicit workflow using GitHub Actions - just by checking a few checkboxes and flipping af few dropdowns on the GitHub Pages setting page of your repo.

This screendump is from the GitHub Pages setting:
<img width="344" alt="image" src="https://user-images.githubusercontent.com/155492/213867908-00a59fa2-bc6a-4ec9-92f9-a2b21292862d.png">

So things are really simplyfied _but_ - there's always a _but_ - this simplification is based on a contract with GitHub: _Your jekyll compiler is limited to what's available in the gem `github-pages`._ A _gem_ is an install package in the _Ruby_ world and the installer is `bundle`. It's equvivalent to _npm-packages_ for _Node.js_ which are installed by `npm`.

This `github-pages` gem comes with a few themes (the layout) as well - and you can apply them simply by mentioning them in the Jekyll configuration file; `_config.yml` file sitting in the root of your Jekyll source. But you use them with the cost that you can't easily modify them. You can say that you managed to separate _what_ from _how_, but you only control the _what_ - the _how_ is applied by sombody else.

This is perhaps good-enough as an MVP, but potentially bad in the long run, for at least two reasons: 1st we would like our layout to be our own, so when people see it they recognize _us_ - not some standard theme - although it's not top-prioority right now, we would like to be able to customize the  theme later on. and 2nd we know that software is never done - and we would probably also want to fix bugs and add features.

Of course Jekyll supports customizable themes (see [jekyllrb.com](https://jekyllrb.com/)). You can either bring it all togeter in to the same repo - all the _how_ along with the _what_. But that is not what we wanted for this repo.  Or you can make you own theme - and that is exacly what is done for this site.

So the now remote Jekyll theme for this repo is [kea-dev/minima](https://github.com/kea-dev/minima) which is initially just a fork of the official jekyll theme [minima](https://github.com/jekyll/minima) but it's already change a bit.

We now have two seperate repos one for _what_ ([this repo](https://github.com/kea-dev/kea-dev.github.io)) and one for _how_ (our own [minima theme fork](https://github.com/kea-dev/minima)). 

We have put the Jekyll source inside a `/docs` folder in the repo and the content - all the markDown files - are in the in the `/docs/posts` folder. We only have very few excess files in the `docs` root: 
 - a 404 landing page
 - an index page
 - an about page.
 - a CNAME file
 - a _config.yml file
 - a .gitignore file.
 - a gem file

The CNAME file tells GitHub pages where the site is hosted. There must exist a DNS CNAME record pointing the site we want our users to visit; [docs.kea.dev](https://docs.kea.dev) which point to an address which by convention is <GITHUB-USER>.github.io - so in our case `kea-dev.github.io` same as this repository name.

The _config.yml is the Jekyll configuration file (see [details](https://jekyllrb.com/docs/configuration/options/))

.gitignore is for the specific `/docs` folder it's a "jekyll - gitignore" file. Whne you run `bundler` and when you build the site, different control files, caches and the static output itself is generated in the same folder - but you don't want all that crab in git - so this file tells git to ignore it.

The gem file is needed for `bundle`to setup a development environment and for building the static site. Technically, you could do without it - but then you would have to rely solely on GitHubs automated build process. So for running a local environment og Jekyll, you do need it.

If you are curious about the details of the bootstrap process for setting all this it up, read through the early issues of the repo and study the commits mentioned in there.

If you are curious about how to join, and setup that Jekyll development locally - head over to the [`CONTRIB.md`](./CONTRIB.md) file and read on.


If you want to report an issue with the site - make yourself heard by creating an [issue](https://github.com/kea-dev/kea-dev.github.io/issues/new/choose)


