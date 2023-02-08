---
layout: post
title:  "Social Coding"
categories: learning
author: lakruzz
links:
  repo:
  slides: 
---

Software development and programming are creative social activities which are supported by technology. GitHub is a social coding platform - It supports modern and contemporary ways of working including principles and concepts adopted from _Agile_, _DevOps_, _Continuous Integration_, _Continuous Delivery_, _Developer Experience_, _Containerization_, _Automation_, _Documentation_ ...
{: .kicker}

<img width="407" alt="image" src="/res/GitHub-logo.png">

# Context
This module is developed in the context of AP programme for Computer Science at Copenhagen School of Technology and Design (KEA). It's part of the fulfillment of the curriculum of the topic [_technology_](https://katalog.kea.dk/course/3050241/2022-2023){: target="_blank"}.

# The Tech Stack
We will be exploring the following technologies:

- GitHub - including 
  - [GH CLI](https://cli.github.com/manual/){: target="_blank"}
  - [CodeSpaces](https://docs.github.com/en/codespaces/overview){: target="_blank"} (and by extension VS Code)
  - [Issues](https://docs.github.com/en/issues/tracking-your-work-with-issues/about-issues){: target="_blank"}
  - [Forks](https://docs.github.com/en/get-started/quickstart/fork-a-repo){: target="_blank"}
  - [Pull Requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request){: target="_blank"}
  - [Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects){: target="_blank"}
  - [Teams](https://docs.github.com/en/organizations/organizing-members-into-teams/about-teams){: target="_blank"}
  - [Discussions](https://docs.github.com/en/discussions/quickstart){: target="_blank"}
- Git (CLI)
  - [Merges and merge strategies](https://git-scm.com/docs/merge-strategies){: target="_blank"}
  - [Git config](https://git-scm.com/docs/git-config){: target="_blank"}
  - [Git Ignore](https://git-scm.com/docs/gitignore){: target="_blank"}
  - [Git Alias](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases){: target="_blank"}
- [Branching strategies](https://www.gitkraken.com/learn/git/best-practices/git-branch-strategy){: target="_blank"}
  
# Learning goals
- Understand and master tools and techniques to support asynchronous, text-based collaboration in a distributed VCS.
- Utilize principles of Social Coding in GitHub through web features, CodeSpace and CLI.

# Resources

## Flipped Classroom
The concept of a [flipped classroom](/posts/flipped-classroom/) is putting the focus on the learner's learning - rather than the instructor's teaching. Familiarize yourself with the resources below - _("suck 'em up!")_ - before we meet in class. It's likely and even expected that the material will raise questions. Should that be the case, you are encouraged join the [KEA.dev discussions 💬](https://github.com/orgs/kea-dev/discussions){: target="_blank"} on GitHub. Feel free to mention or assign me - [@lakruzz](https://github.com/lakruzz) - if you post a question. 


## GitHub Projects and Issues
📚 [Project Planning for Developers](https://github.com/features/issues/){: target="_blank"}<br/>
⏱️ [20:00]

This is a link to GitHub's official introduction to projects - it's very high-level and may not actually bring you much learning. But use it as a strating point for your exploration of GitHub Projects. Dive into the frequently asked questions (at the bottom of the page) or try to explore the topic in another way (try using the link in [The Tech Stack](#the-tech-stack) list above - it points to the manual). Time box this to at least 20 mins - familiarize yourself with GitHub Projects - what at they trying to help you with? Try it out in one of your own repositories.

## Git Branching strategies
📚 [1: Branching strategies](https://www.gitkraken.com/learn/git/best-practices/git-branch-strategy){: target="_blank"}<br/>
⏱️ [30:00]<br/>

📚 [2 Trunk based development ...](https://www.atlassian.com/continuous-delivery/continuous-integration/trunk-based-development){: target="_blank"}<br/>
⏱️ [30:00]<br/>

[1<sup>st</sup> link](https://www.gitkraken.com/learn/git/best-practices/git-branch-strategy){: target="_blank"} is a short piece on branching strategies - it introduces three different flows: _"Git Flow"_, "GitHub Flow"_ and "GitLab Flow"_ see if you can grasp them - and how they differ.

In the old days (ten-fifteen years ago) branching strategies were really a _hot topic_ - and it wasn't easy. Today there seem to be a convention among most teams that some variant of keeping the _master_ (a.k.a _trunk_ or _main_) pristine and ready for deploy is the way to go. This concept too has many names; _trunk-based development_ (derives from an old - now obsolete version control system called Subversion), or _Release Train_ which comes from SAFe - a framework that claims tha Agile can scale. Read about Trunk-based developement it in [the 2<sup>nd</sup> link](https://www.atlassian.com/continuous-delivery/continuous-integration/trunk-based-development){: target="_blank"}.  And the ask yourself? Is _GitHub Flow_ compliant with the concept of "trunk based development"? Is _Git Flow?_

<script type="text/javascript" src="https://ssl.gstatic.com/trends_nrtr/3197_RC04/embed_loader.js"></script> <script type="text/javascript"> trends.embed.renderExploreWidget("TIMESERIES", {"comparisonItem":[{"keyword":"/m/05vqwg","geo":"","time":"2004-01-01 2023-02-08"},{"keyword":"/m/012ct9","geo":"","time":"2004-01-01 2023-02-08"},{"keyword":"/m/0ryppmg","geo":"","time":"2004-01-01 2023-02-08"}],"category":0,"property":""}, {"exploreQuery":"date=all&q=%2Fm%2F05vqwg,%2Fm%2F012ct9,%2Fm%2F0ryppmg","guestPath":"https://trends.google.com:443/trends/embed/"}); </script>

The graph above is just for fun - git is disruptive - literally. It killed Subversion! And GitHub is now more popular and used - than git itself. _The tail wagging the dog?_

## KanBan - Signalling board
📺 [1: Atlassian's take on KanBan](https://www.youtube.com/watch?v=iVaFVa7HYj4){: target="_blank"}<br/>
⏱️ [06:00]<br/>

📚 [2: Scrum/KanBan difference](https://miro.com/blog/scrum-kanban-boards-differences/){: target="_blank"}<br/>
⏱️ [15:00] (read time), 📺 [11:00] (three embedded videos)<br/>

We touched briefly on KanBan earlier. The method is old (1980'ies) - it derives from "TPS - Toyota Production System" - Lean Manufacturing. To many it's seen as an alternative method to Scrum. Luckily KanBan is merely a technique and Scrum is (sometimes) a methodology - not (always) a religion - so you are free to combine them if you got the stomach for it.

Watch [Atlassian's take on KanBan](https://www.youtube.com/watch?v=iVaFVa7HYj4){: target="_blank"} - and [Miro's explanations of the difference](https://miro.com/blog/scrum-kanban-boards-differences/){: target="_blank"} between KanBan and Scrum.

<iframe width="560" height="315" src="https://www.youtube.com/embed/iVaFVa7HYj4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

What are your thoughts? any preferences?

# Additional resources

This section gives you more - but on a strictly volunteer basis. Continue to explore if you like. But in order to tag along in class, the resources above are sufficient.

## Git Aliases - taken to extreme
🔍 ["Git Aliases - taken to extreme"](https://www.inc-inc.dk/stories/git-aliases/){: target="_blank"}<br/>
⏱️ [20:00]<br/>

This is a blog I wrote to demonstrate some nifty git tricks - and it also explains the concept of SemVer - Semantic Versioning. As the title says it's a bit extreme - so I put it under additional resources.

## GitHub CoPilot
🔍 [CoPilot - OpenAI Codex](https://github.com/features/copilot){: target="_blank"} and [GitHub Copilot Docs](https://docs.github.com/en/copilot){: target="_blank"}<br/>
⏱️ [30:00]<br/>

You know ChatGPT right?  You've head all the stories about how it can write you code for you. But did you also know that the same AI engine - _codex_ which is an integrated part of _OpenAI_ is also available as an extension to VS Code? Check it out. Install it, play with it - and then ask yourself is this cheating? Is it helpful? If this is how code is written in the future - where does that leave us - as programmers? Time box this to at least 30 mins
