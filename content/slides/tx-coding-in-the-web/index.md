---
title: Coding inside the web browser! Talking about GitHub Codespaces and Gitpod.
date: "2022-05-15T19:33:20Z"
url: "/slides/tx-coding-in-the-web/"
image: "/talks/that-logo-tx-22.svg"
description: "Slides for THAT Conference TX 2022 session about coding inside a web browser."
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
## An introduction to Gitpod and GitHub Codespaces

???

We're online, so I hope you're in the right place! We can do some banter, but mute yourself during the presentation unless you're trying to ask a question.
---
background-image: url(that/01-TX-THAT-Conference-Branding.png)
background-size: cover

???

# Welcome to THAT Conference Texas: 2022!

- If you're in Texas, that's great!  Type where you're watching from in the chat! I'm presenting from Wisconsin.
- Background images don't appear to scale correctly unless I also apply "background-size: cover" to the slide.-

---
background-image: url(that/02-TX-THAT-Conference-Partners.png)
background-size: cover

???
# Sponsors 

- Sponsors are great.  Without them, That Conference would not be possible.
- This year in particular, I'm thankful for the companies that stuck their neck out for the first year of THAT in TX.
- [Unspecified](https://unspecified.io/)
- [Improving](https://improving.com/)
- [Progress](https://www.progress.com/)
- [Oracle](https://www.oracle.com/index.html)

---
background-image: url(that/03-TX-THAT-Dates.png)
background-size: cover

???

It's not too early to think about next year in Texas! In fact, start thinking of some topics, because the call for speakers starts June 1st!

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

Important to note here: 
The coding usually I do in my free time is:
-  Hugo Static sites and 
- .NET Core apps, usually webscrapers.
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

The history of web IDEs seems pretty sparse on the web, but things started more than ten years ago.

The earliest cloud IDEs I can find references to are eXo Cloud IDE and Cloud9 IDE between 2009-2011.

---
class: col-2

# Early Drawbacks

- Language support
- Performance and Crashes
- Source Code Management
- Features/Debugging

![that-animal](misc/angry-error.jpg)

???

- Coding was often processed using Javascript.
- Language support was rudimentary, 
- performance was subpar, 
- accidentally refreshing the page may cause things to crash or reset
- source code managment integration was often missing, 
- and debugging was very difficult, if not impossible.

Because of the poor developer experience, especially for "non-web" languages, few developers coded using web IDEs at the start.
But, time passes, and things get better. Let's skip the middle and fast-forward to now.
---
class: img-right
![that-animal](that/octopus_with_flag_that.png)

## Modern coding in the browser

Different tools for different goals
- Language Learning 
- Code Interviews
- Notebooks
- Write and Publish
- Collaboration-first 
- Enterprise and Cloud Focused
- Repository Superchargers

???

There's a bunch of stuff now in different flavors.

Companies are still trying to figure out what people want (and will pay for).

I'm going to divide everything into roughly seven categories, and explain the goals of each.
- Language Learning 
- Code Interviews
- Notebooks
- Write and Publish
- Collaboration-first 
- Enterprise and Cloud Focused
- Repository Superchargers
---
class: img-caption
![trydotnet](misc/trydotnet-that.png)
# Language learning 

???

# Language learning 
Stuff made to either learn languages in a directed fashion or test snippets of language you make.

Examples:
- ["Fiddle" tools](https://fiddles.io/) 
- [Try dot net](https://dotnet.microsoft.com/platform/try-dotnet)
- [REPLit.com](https://replit.com/~)
- [Codingground](https://www.tutorialspoint.com/codingground.htm)

---
class: title, smokescreen, shelf, no-footer
background-image: url(misc/coderpad-ide-screenshot.jpg)

# Code Interviews
???
# Code Interviews
Coding tools made to record behavior and test knowledge for evaluation.

Basically, a next gen whiteboard for interviews.
- [CodeBunk](https://codebunk.com/#)
- [CoderPad](https://coderpad.io/)

---
class: img-caption
![jupyter](misc/jupyter-try.png)
# Notebooks
???
# Notebooks

Tools made to share data or calculations and the code used to find the results 
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
# Write and Publish
Web tools whose main goal is to streamline the creation and publishing process, often in a "playground" subdomain. Allows "remixes".
- [Glitch](https://glitch.com) - recently acquired by [Fastly](https://www.fastly.com/blog/fastly-announces-acquisition-of-glitch-a-future-of-yes-code-at-the-edge)
- [WebContainers](https://blog.stackblitz.com/posts/introducing-webcontainers/)
---
class: title, smokescreen, shelf, no-footer
background-image: url(misc/duckly-landing-demo.gif)

# Collaboration-first 
???
# Collaboration-first 
Tools that prioritize collaboration and mentoring over everything else. 
Has audio/video, and simultaneous control
- [Duckly](https://duckly.com/)
---
class: title, smokescreen, shelf, no-footer
background-image: url(misc/google-cloud-shell.gif)
# Enterpise and Cloud Service IDEs

???

# Enterpise and Cloud Service IDEs

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
- [Microsoft Dev Boxes](https://techcommunity.microsoft.com/t5/azure-developer-community-blog/introducing-microsoft-dev-box/ba-p/3412063)
---
class: col-2
# Repository Superchargers
Gitpod
![gitpod](gitpod/gitpod-opening-repo-5.gif)
![gitpod](gitpod/open-with-gitpod.svg)

GitHub Codespaces
![codespaces](github/codespaces.gif)
![codespaces](github/open-with-codespaces.png)

???
# Repository Superchargers

My final category.

These are tools that make working with open source repositories easier. 

They open your repo in a customizable docker container that can allow you functionality that usually comes only on desktop IDEs.

There's also a streamlined commit and push process.


- [Gitpod](https://www.gitpod.io/)
- [GitHub Codespaces](https://github.com/features/codespaces)

Here's what I'm going to talk about today.
---
# How are Gitpod and Codespaces similar?

- Broad language support, auto-complete, intellisense
- Configurable color themes
- Integrated debugger
- Integration with GitHub repositories
- Free tier available
- Uses Visual Studio Code*
- Allows VS Code Extensions*
- iPad support
- VNC Support

???
# How are Gitpod and Codespaces similar?

There are quite a few similarities between the two products.  

If you use one, it shouldn't be hard to use the other.

Both use VS Code by default, integrate with GitHub, and offer some pretty nice language support.

They can also be customized with different color themes and extensions.
---
# Gitpod and Codespaces - Differences


| Gitpod ![gitpod](gitpod/open-with-gitpod.svg)     | Codespaces  ![codespaces](github/open-with-codespaces.png)                    |
|---------------------------------------------------|-------------------------------------------------------------------------------|
| Support for GitHub, GitLab, and Bitbucket         | GitHub-only                                                                   |
| Open for sign-ups, use right away                 | Private beta with sign-up page                                                |
| Released product with pricing and free tier       | Free, "for now" while in beta                                                 |
| Collaboration through shared workspace or snapshot| Visual Studio Live-share                                                      |
| No integration with AI Copilot                    | Integrates with AI Copilot (beta), but you have to be in both beta programs   |
| Local IDE connection in preview                   | Can connect to a local install of VS Code                                     |
| You can self-host on kubernetes                   | Not available to self-host                                                    |


???
# Gitpod and Codespaces - Practical Differences

- Gitpod has support for GitHub, GitLab, and Bitbucket. Codespaces is limited to GitHub.
- Gitpod has been around since 2018 with a userbase and published pricing. Codespaces is still in beta as of 2021, though it is free if you can get in via the [sign-up page](https://github.com/features/codespaces/signup).
- Collaboration in Codespaces is done with VS Live Share. Gitpod handles collaboration via shared workspaces, or by creating shareable snapshots.
- Codespaces integrates with AI Copilot(beta) via a VS Code Extension, but you have to be accepted into both beta programs. Copilot is not available for Gitpod.
- There's a VS Code extension to allow you to connect a local install of VS Code GitHub Codespaces. Gitpod is working on connecting to local IDEs with [Gitpod Local Companion](https://www.gitpod.io/docs/develop/local-companion), but it is still in preview.
- If you're motivated, you can self-host Gitpod on kubernetes. It's not currently possible with Codespaces (though VS Codespaces did have that option).

---
# Gitpod and Codespaces - Philosophy
| Gitpod ![gitpod](gitpod/open-with-gitpod.svg)     | Codespaces  ![codespaces](github/open-with-codespaces.png)                    |
|---------------------------------------------------|-------------------------------------------------------------------------------|
| Open-Source                                       | Proprietary                                                                   |
| VS Code - Open Source Version                     | VS Code - Proprietary version                                                 |
| VS Code Extensions - Open VSX Registry            | VS Code Extensions - Extension Marketplace                                    |
| Ephemeral (built fresh every time)                | Only rebuilds image on config change (starts existing VM)                     |
| Prebuilds - allows precompiling certain items     | Rebuilds from scratch based on config                                         |
| Tasks - Run commands before opening IDE           | Does not appear to support running commands before opening                    |

???
# Philosophical Differences

- Gitpod is [open-source](https://github.com/gitpod-io), Codespaces is proprietary.
- While [VS Code is open source](https://github.com/microsoft/vscode), Codespaces uses a proprietary version of VS Code.
- Extensions also work differently, Microsoft has the proprietary [Extension Marketplace](https://marketplace.visualstudio.com/), Gitpod uses the [Open VSX Registry](https://open-vsx.org/)
- Gitpod environments are designed to be ephemeral, rebuilt every time you need one. Codespaces seems to keep your container handy, and restarts it when you need it again, only rebuilding if you change the configuration of the container.
- Gitpod has an option to offload some of the compilation process outside of the startup process in what they call "Prebuilds".  That seems cool.
- Gitpod also allows you to run tasks, like restoring packages or running commands before the web IDE starts.  I'm not aware of Codespaces being able to do this.
---
class: img-caption
![demo](misc/orville.gif)
 # Demos!

???
Enough talking. Let's do a demo of Gitpod and Codespaces.

Note: I'm not starting these virtual machines from scratch.  That seems like a disaster waiting to happen.

---
class: img-caption
![demo](gitpod/gitpod-example.gif)

# Gitpod

???
- Show off Hugo site.
- Change color themes
- Show .gitpod.Dockerfile and .gitpod.yml 
- Note that "tasks" allow running a hugo server automatically

---
class: img-caption
![demo](github/codespaces-example.gif)

# GitHub Codespaces

???
- do dotnet restore
- Show off debugging.
- Show off Copilot.
- Show devcontainer.json file and Dockerfile
---
class: title, smokescreen, shelf, no-footer
background-image: url(that/bigfoot-with-that-badge.png)

# Should I use Gitpod or Codespaces?


???

Should I use Gitpod or Codespaces?
---
background-image: url(misc/both2.gif)
background-size: cover

???

Which one should you use? Maybe both of them? I'd certainly suggest trying Gitpod first, since you don't have to wait to do it. I certainly prefer it when working on Hugo Static Sites.

However, Codespaces is nice, too. Since GitHub is a Microsoft product, any new GitHub features may come to Codespaces first, though they may come in beta signup form like AI Copilot.

Both products are still under active development, so I would encourage you to pay attention to both Gitpod and Codespaces as they continue to add features and improve.
---
class: img-caption
![thinking](misc/thinking.gif)

# Questions?

???

# Any Questions?
---
background-image: url(misc/thankyou.webp)
background-size: cover

???

# Thanks!
---
 # Credits

- THAT Conference Cartoons courtesy of THAT Conference, © 2021 THAT® All rights reserved.
- "Demo" gif of Yaphit doing tech support comes from "The Orville" created by Seth MacFarlane. RIP, Norm MacDonald.
- "Both" gif is from "The Road To El Dorado", Directed by Bibo Bergeron and Don Paul
- "Looking let me think" gif courtesy of TipsyElves.com
- "Thank you" gif is from Super Mario World, Ending screen
- Web IDE screenshots courtesy of their respective sites.