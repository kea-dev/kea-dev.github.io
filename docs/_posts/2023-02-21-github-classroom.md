---
layout: post
title:  "GitHub Classroom assignments"
categories: github vscode training
author: lakruzz
---
Most training modules listed here on docs.kea.dev uses GitHub Classroom Assignments - for in-class exercises. This post is a short introduction to the ground rules and how it's used. Read it if you haven't accepted a GitHub Classroom Assignment before.
{: .kicker}

#  Classroom assignments

The modules here on [docs.kea.dev](/) have [GitHub Classroom](){: target="_blank"} assignment. The assignments are based on GitHub repositories. 

An assignment is based is based on a template repository. When you accept an assignment a GitHub repository is created as a copy from the template. It's not a_clone_, it's not a _fork_. It's a detached _copy_ - it doesn't share any history with the template repository.

- In _group assignments_ you share a repository among the group.
- In _individual assignments_ you get your own repository.

To accept an assignment you will need an invitation link (usually available in the module description). 


# Don't be a stranger
The assignments are most often supplement to a [flipped classroom](posts/flipped-classroom/) approach - it means that we will do these exercises in class together where you can get support: Instructors can support learners - and learners can support each other.

The exercises are _not_ designed to be _homework_ - but if you aren't able to join class, then you should work your way through them.

# Ground rules
A few words on the assignments:

#### Rule #1: VS Code
The assignments are designed to be worked in VS Code. Either as a desktop application or an online version.

#### Rule #2: Linux terminal
The assignments are designed to have access to a linux bash'ish shell terminal 

&nbsp;&nbsp;👍 A CodeSpace on GitHub (recommended)<br/> 
&nbsp;&nbsp;👍 A PC running a Linux distro<br/> 
&nbsp;&nbsp;👍 The terminal on Mac<br/> 
&nbsp;&nbsp;👍 WSL on Windows<br/>
&nbsp;&nbsp;👍 A Docker container on either Windows or Mac<br/>

&nbsp;&nbsp;👎 GitBash on Windows won't work 

#### Rule #3: git and GitHub CLI
The assignments uses git and the [GitHub CLI](https://cli.github.com/){: target="_blank"} `gh`. It must be properly installed and authenticated.

To test if your're good to go, open the terminal and run :

```shell
gh auth status
```
It should run flawlessly and verify that your are logged in to GitHub.

**Note on Rules 1-3** : The assignments are developed and tested in a GitHub CodeSpace; which out of the box supports all of rules 1 through 3. So do your exercises in a GitHub CodeSpace and you'll be fine!

#### Rule #4: Work those issues
The actual tasks/exercises are given to you as _issues_. If there aren't any issues in the repo yet, you must initiate your repo _once_. The repository itself contains the script that will copy the issues over from the template - here's how:

- Open a terminal from the root of your repository and run:
```shell
./github/template/cpissues.sh
```

#### Rule #5 Build a portfolio
Think of these assignments as you - building your own portfolio. You are encouraged to log you progress, findings, questions etc. by a combination of: 
- commenting on the issues
- making notes in the `README.md` file
- create more MarkDown files (_any_ file wit a `.md` extension). 

Leave a trace for yourself to follow. Then you can always find your way back!

# Automated workflows
Most of the assignments are setup using _auto grading_ features.

Every time you push to GitHub the _GitHub Actions_ kicks in and starts a workflow that will test if your repository is in the expected state. You can always go and check the status on you most recent push at the _"Actions"_ tab on you repository at GitHub.

<img width="200" align="right" alt="image" src="https://user-images.githubusercontent.com/155492/220343689-b5d8aae6-a6c7-400d-bdfe-94546ac992f8.png"> You are interested in the Job called _"Autograding"_ defined in `classrooms.yml` Click and expand the job and locate the step named _"Run education/autograding..."_

Every time you push to GitHub it runs again - so if something is broken, go back to your repo, fix the issue and git `add` + `commit` + `push` 

If you would like to run the tests in the autograding action locally - before you commit then have a look at the `classroom.yml`. 

Run in terminal:
```shell
cat .github/classroom/autograding.json
```

You see each step has a `run:` clause - could look like this:

```json
      {
        "name": "Test if push.default is set in .gitconfig",
        "setup": "",
        "run": ".github/classroom/pushdefault.sh",
        "input": "",
        "output": "",
        "comparison": "included",
        "timeout": 10,
        "points": 25
      }   
```

To run the test locally in you repo, simply copy whatever the `run` clause does and execuute it from the terminal - example from above:

```shell
.github/classroom/pushdefault.sh
```

**NOTE:** Sometimes a test deliberately alters the state of the repository for the next test to take over - so a given test _can_ be dependant on the previous test has run.

...you'll figure it out!

# Getting help 

#### The issues in the assignments
Each Github assignment is based on issues - exploit that to ask the questions or requests for help directly in the comments on the individual issues - be sure to mention either me [@lakruzz](https://github.com/lakruzz){: target="_blank"} or one of your fellow students - and a notification will be sent to the person you mentioned. If you are stuck - escalate by _assigning_ that person to your own issue. 

#### Discussions at the kea-dev organization on GitHub
If you're alone - and your're stuck you can go to the [discussions at kea.dev on GitHub](https://github.com/orgs/kea-dev/discussions){: target="_blank"}. Be aware that it's an open discussion forum - anyone can join, anyone can see your questions and posts and anyone can reply and comment. 

It's much like [Stack Overflow](https://stackoverflow.com/){: target="_blank"} but in a KEA _safespace_ 👷. 


#### Me - solving my own assignments
To some of the assignments I've recrecorded myself solving my own issues - if that is the case, then the videos will be available on the modul's pos on [docs.kes.dev](/).
---
