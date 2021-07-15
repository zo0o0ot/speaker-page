---
title: Coding inside the web browser! Talking about GitHub Codespaces and GitPod.
date: "2021-06-27T19:33:20Z"
url: "/slides/coding-in-the-web/"
image: "/talks/that_conference_10yr_logo.svg"
description: "Slides for THAT Conference 2021 talk about coding inside a web browser."
ratio: "16:9"
themes:
- apron
- adirondack
- descartes
classes:
- feature-qrcode
---
class: title, smokescreen, shelf, no-footer
background-image: url(gitpod/coding-web-gitpod-screenshot.png)

# Coding in the Web
## An introduction to GitPod and GitHub Codespaces

???

Make sure you're in the right room!
---
background-image: url(that/That-Conference-Branding-Slide.png)
background-size: cover

???

Temporary Branding slide- 2021 slide TBD

Welcome to THAT Conference

- Background images don't appear to scale correctly unless I also apply "background-size: cover" to the slide.-

---
background-image: url(that/That-Conference-Sponsors-Slide.png)
background-size: cover

???

Temporary Sponsors slide- 2021 slide TBD

Sponsors are great.  Without them, That Conference would not be possible.  I'm thankful for them.

---
background-image: url(that/That-Conference-2020.png)
background-size: cover

???

Temporary Future Dates slide- 2021-2022 slide TBD

Please consider coming back next year. Here are the dates!

---
class: img-left
# About Me

![Selfie](ross1.jpg)

- Software Developer at Paradigm
- Luther College Alumnus
- Admin, [Madison, WI Slack](http://madisoncommunity.org/)
- Father
- Gamer
- Sports fan
- Survivor

@rosslarsonWI

hello@rosslarson.com

THAT Slack : rosslarson

???

Hi. I'm Ross.

I'm a father, a gamer, a sports fan, a geek, and other stuff.
---
# Slides and Session Information

.qrcode.db.fr.w-40pct.ml-4[]

- General session info available at https://rosslarson.com/talks/
- Slides are at https://rosslarson.com/slides/ or just use the QR code
- Ask questions anytime

???

Here's a QR Code if you want to follow along on your laptop or phone.
Ask questions anytime.
---
class: img-left
![that-animal](that/moose_with_lantern_that.png)

# Writing code in the web browser.

A history.
???
So, Coding in the web. It's a thing.
History of web IDEs seems pretty sparse on the web, but things started about ten years ago.
The earliest cloud IDEs I can find references to are eXo Cloud IDE and Cloud9 IDE between 2009-2011.
---
class: col-2

# Early Drawbacks

- Language support
- Performance
- SCM
- Features/Debugging

![that-animal](misc/angry-error.jpg)

???

- Language support was rudimentary, 
- performance was subpar, 
- source code managment integration was usuoftenally missing, 
- and debugging was very difficult, if not impossible.

Because of the poor developer experience, few developers coded using web IDEs at the start.
But, time passes, and things get better. Let's skip the middle and fast-forward to now.
---
class: col-2


# Modern coding in the browser

Different tools for different goals
- Language learning 
- Code Interviews
- Notebooks
- Write and publish
- Collaboration-first 
- Fuller featured IDEs
- Repo superchargers

![that-animal](that/octopus_with_flag_that.png)
???

There's a bunch of stuff now in different flavors, although you can tell people are still trying to figure out what people want.
I'm going to divide them into roughly six categories.
- Language learning 
- Code Interviews
- Notebooks
- Write and publish
- Collaboration-first 
- Enterprise and Cloud Service IDEs
---
class: img-caption
![trydotnet](misc/trydotnet-that.png)
# Language learning 

???

Stuff made to either learn languages in a directed fashion or test snippets of language you make.

Examples:
- ["Fiddle" tools](https://fiddles.io/) 
- Try dot net
- REPLit.com
- Codingground

---
class: title, smokescreen, shelf, no-footer
background-image: url(misc/coderpad-ide-screenshot.jpg)

# Code Interviews
???

Coding tools made to record behavior and test knowledge for evaluation

Basically, a next gen whiteboard for interviews.
- [CodeBunk](https://codebunk.com/#)
- [CoderPad](https://coderpad.io/)

---
class: img-caption
![jupyter](misc/jupyter-try.png)
# Notebooks
???

Tools made to share data and the work used to reach the results 
- data science/visualization
- [Jupyter](https://jupyter.org/try)
- R
- Julia
- [Observable (JS)](https://observablehq.com/)
---
class: title, smokescreen, shelf, no-footer
background-image: url(misc/glitch-1.gif)
# Write and Publish
???

Tools whose main goal is to streamline the publishing process, often in a "playground" subdomain. Allows "remixes".
- [Glitch](https://glitch.com)
---
class: title, smokescreen, shelf, no-footer
background-image: url(misc/duckly-landing-demo.gif)

# Collaboration-first 
???

Tools that prioritize collaboration and mentoring over everything, audio/video, simultaneous control
- [Duckly](https://duckly.com/)
---
class: title, smokescreen, shelf, no-footer
background-image: url(misc/google-cloud-shell.gif)
# Enterpise and Cloud Service IDEs

???

- Web IDEs focusing on delivering features to enterprises
- You may be able to configure the cloud provider you use for your virtual machine, or self-host
- Cloud IDEs making it easier to buy cloud services (AWS Lambda functions, GCP)


~~

- [AWS Cloud 9](https://aws.amazon.com/cloud9/)
- [Google Cloud Shell](https://cloud.google.com/shell/)
- [Codiad](http://codiad.com/)
- [Koding](https://www.koding.com/)
- [CodeAnywhere](https://codeanywhere.com/)
- [GoormIDE](https://ide.goorm.io/)
---
class: col-2
# Repository Superchargers
GitPod
![gitpod](gitpod/gitpod-opening-repo-5.gif)
![gitpod](gitpod/open-with-gitpod.svg)

GitHub Codespaces
![codespaces](github/codespaces.gif)
![codespaces](github/open-with-codespaces.png)

???

These are tools that make working with open source repositories easier. They open your repo in a customizable docker container that can allow you functionality that usually comes only on desktop IDEs.

- [GitPod](https://www.gitpod.io/)
- [GitHub Codespaces](https://github.com/features/codespaces)

Here's what I'm going to talk about today.
---

# How are GitPod and Codespaces similar?

- Broad language support, auto-complete, intellisense
- Configurable color themes
- Integrated debugger
- Integration with GitHub repositories
- Free tier available
- Uses Visual Studio Code
- Allows VS Code Extensions
- iPad support
- VNC Support

---
# How are GitPod and Codespaces different?


| GitPod ![gitpod](gitpod/open-with-gitpod.svg)     | Codespaces  ![codespaces](github/open-with-codespaces.png)                    |
|------------------------------------------------|----------------------------------------------------------------------------------|
| Open-Source                                       | Proprietary                                                                   |
| Support for GitHub, GitLab, and Bitbucket         | GitHub-only                                                                   |
| Open for sign-ups, use right away                 | Private beta with sign-up page                                                |
| Released product with pricing and free tier       | Beta.  Free, "for now".                                                       |
| Collaboration through shared workspace or snapshot| Visual Studio Live-share                                                      |
| No integration with AI Copilot                    | Integrates with AI Copilot (beta), but you have to be in both beta programs   |
| Local IDE connection in preview                   | Can connect to a local install of VS Code                                     |
| You can self-host on kubernetes                   | Not available to self-host                                                    |


???

- GitPod is [open-source](https://github.com/gitpod-io), and while [VS Code is open source](https://github.com/microsoft/vscode), not everything in Codespaces is.
- GitPod has support for GitHub, GitLab, and Bitbucket. Codespaces is limited to GitHub.
- GitPod has been around since 2018 with a userbase and published pricing. Codespaces is still in beta as of 2021, though it is free if you can get in via the [sign-in page](https://github.com/features/codespaces/signup).
- Collaboration in Codespaces is done with VS Live Share. Gitpod handles collaboration via shared workspaces, or by creating shareable snapshots.
- Codespaces integrates with AI Copilot(beta) via a VS Code Extension, but you have to be accepted into both beta programs. I'm only in one. Also, it doesn't show up in the list of VS Code Extensions in GitPod
- There's a VS Code extension to allow you to connect a local install of VS Code GitHub Codespaces. GitPod is working on connecting to local IDEs with Gitpod Local Companion, but it is still in preview.
- If you're motivated, you can self-host GitPod on kubernetes. It's not currently possible with Codespaces (though VS Codespaces did have that option).

I'm not sure if prebuilds are a topic of conversation here.

---
class: img-caption
![demo](misc/orville.gif)
 # Demos!

???
Let's look at GitPod and Codespaces.
TODO: Specific examples of environment advantages, like Hugo autostarting the server.
---
class: title, smokescreen, shelf, no-footer
background-image: url(that/bigfoot-with-that-badge.png)

# Should I use GitPod or Codespaces?


???

Should I use GitPod or Codespaces?
---
background-image: url(misc/both2.gif)
background-size: cover

???

Which one should you use? Maybe both of them? I'd certainly suggest trying GitPod first, since you don't have to wait to do it. 

However, Codespaces is nice, too. Since GitHub is a Microsoft product, any new GitHub features may come to Codespaces first, though they may come in beta signup form like AI Copilot.

---
class: img-caption
![thinking](misc/thinking.gif)

# Questions?

---
background-image: url(misc/thankyou.webp)
background-size: cover

???

Thanks!
---
 # Credits

- THAT Conference Cartoons courtesy of THAT Conference, © 2021 THAT® All rights reserved.
- "Demo" gif of Yaphit doing tech support comes from "The Orville" created by Seth MacFarlane
- "Both" gif is from "The Road To El Dorado", Directed by Bibo Bergeron and Don Paul
- "Looking let me think" gif courtesy of TipsyElves.com
- "Thank you" gif is from Super Mario World, Ending screen
- Web IDE screenshots courtesy of their respective sites.
