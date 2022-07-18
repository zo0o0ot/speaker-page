---
title: Getting (.NET) Interactive! Slides for THAT Conference 2022 session about .NET Interactive.
date: "2022-06-14T19:33:20Z"
url: "/slides/getting-net-interactive/"
image: "/talks/that_conference_10yr_logo.svg"
thumbnail: "/talks/images/that-logo-states-wi.svg"
description: "Slides for THAT Conference 2022 session about .NET Interactive."
ratio: "16:9"
themes:
- apron
- adirondack
- descartes
classes:
- feature-qrcode
---
class: title, smokescreen, shelf, no-footer
background-image: url(images/dotnet-interactive.png)

# Getting (.NET) Interactive!
## An introduction to .NET Interactive Notebooks

???

Make sure you're in the right room!
---
background-image: url(that/That-Conference-Branding-Slide.png)
background-size: cover

???

# Welcome to THAT Conference 2022!

- Background images don't appear to scale correctly unless I also apply "background-size: cover" to the slide.-

---
background-image: url(that/That-Conference-Partners-Slide.png)
background-size: cover

???
# Sponsors 

Sponsors are great.  Without them, That Conference would not be possible.  I'm thankful for them.

---
background-image: url(that/THAT.us.png)
background-size: cover

???

That.us is pretty great.  Come and join the conversation, all year long!

---
background-image: url(that/THAT-Dates.png)
background-size: cover

???

Also.... It's never to early to start thinking about next year!

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
- .NET Core apps, often webscrapers.
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
class: top
# A history of working with .NET interactively.
![helloWorld](images/helloWorldTutorial.png)

???

Dotnet has been around for a while, but trying it out used to involve quite a few steps, such as:
- Downloading and installing Visual Studio
- Installing a dotnet SDK
- Creating a project or app
- Running or debugging the program to see output.

It was the way things were always done, but there was certainly room for improvement.
---
class: col-2

# Drawbacks to Traditional .NET in Visual Studio

- Big initial download and setup
- Initial output is mostly limited to debugging and print statements
- Hard to share results of code

![sad-dog](images/sadDog.png)

???

- The initial setup of Visual Studio can be daunting.  The install size for Visual Studio Community including suggested SDKs and tools is about 30-50 GBs nowadays.
- Getting past the initial "Hello World" phase can take some time, and your early output is going to probably be print statements and looking at variables in immediate window while debugging.
- Visual Studio isn't really built to store the output of the code you write, as it was written with development of the application in mind, not necessarily the output.

---
class: img-caption
![trydotnet](images/trydotnet-that.png)

## The first big step - Try.NET in the browser

???

- In 2019, .NET started to move foward to the web in a new way.
- A REPL (Read-Eval-Print Loop) isn't a new concept, but because C# did not start as a web language, it wasn't close to the first language
- Try dot net in the browser was a pretty big step for the .NET stack.
- Apparently, at the start, Microsoft was footing the bill for azure virtual machines that were connecting with every site visitor that wanted to try dotnet in the browser.
- Eventually, Blazor allowed them to save on some server costs.
---
class: img-caption
![try-dotnet-example](images/dotnet-try2.gif)

# `dotnet try` - Creating your own interactive documentation

???

- The website was cool, and it allowed for experimentation, but what about if you wanted to make something interactive for yourself, or someone else?
- The dotnet try tool allows you to match markdown and editable, executable code to be created and served up for yourself or someone else.
- A good example of this is the [hello world](https://docs.microsoft.com/en-us/dotnet/csharp/tour-of-csharp/tutorials/hello-world) tutorial on the Micosoft docs site.

---
class: col-2
# Running `dotnet try` locally

![Dotnet-try-browser](images/dotnet-try.gif)
- Run `dotnet try` from the console 
- (or server)

![Dotnet-try-browser](images/try-markdown.png)
- Markdown mixed with code
- Friendly presentation
- Code is editable by end-user

???

- If you run `dotnet try` locally, it will start a webserver and serve the content into a browser, where you can interact with code blocks and see their results.
- `dotnet try` is pretty cool, but it still requires the user to run the program themselves.
- Also, you run the risk of things running differently on their computer if different packages or versions of things are installed.


---
class: img-caption
![Jupyter](images/jupyter.svg)
# Meanwhile, an (old?) new tool appears from a different land....

???

# Jupyter - a different tool for a different purpose

Jupyter Notebook (formerly IPython Notebooks) is a web-based interactive computational environment for creating notebook documents.

A Jupyter Notebook document is a browser-based REPL containing an ordered list of input/output cells which can contain code, text (using Markdown), mathematics, plots and rich media. Underneath the interface, a notebook is a JSON document, following a versioned schema, usually ending with the ".ipynb" extension. 

The project was original brought together to support Julia, Python, and R and help those languages create easily consumable and reproducable content.

---
class: img-caption
![VS-Code-Insiders](images/VS-Code-Insiders.png)

# Also Emerging: Visual Studio Code
???
# Visual Studio Code
- Visual Studio Code came out in 2015, [and has been evolving rapidly, as well](https://en.wikipedia.org/wiki/Visual_Studio_Code).
- Their extensions marketplace has allowed for rapid evolution of the tool.

---
class: col-2
# Now........ Let our powers combine!

- ![vs-code](images/vscode.svg# maxw-2) Visual Studio Code
- ![jupyter](images/jupyter.svg# maxw-2) Jupyter Notebooks
- ![dotnet-interactive](images/dotnet-interactive.png# maxw-2) .NET Interactive
- ![OpenSource](images/GitHub-Mark-64px.png# maxw-2) Open Source
- ![heart](images/8bitheart.jpg# maxw-2) Heart

![CaptainPlanet](images/LetOurPowersCombine.gif)

???
# Notebooks are a combination of several powers

- Because of the beauty of open source, a rising tide lifts all boats
- Microsoft was able to add a .NET Interactive Kernel into Jupyter Notebooks.
- Microsoft then added .NET Notebooks support
    - First to VS Code (and [nteract](https://nteract.io/), and Azure Data Studio)
    - Then to visual Studio

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
- Picutre of a sad dog courtesy of user pinoyed on flickr. Image description: Murray's sad face. - Creative Commons Attribution 2.0 Generic (CC BY 2.0) - https://www.flickr.com/photos/pinoyed/5009440499/in/photostream/
- "Demo" gif of Yaphit doing tech support comes from "The Orville" created by Seth MacFarlane
- "Both" gif is from "The Road To El Dorado", Directed by Bibo Bergeron and Don Paul
- "Looking let me think" gif courtesy of TipsyElves.com
- "Thank you" gif is from Super Mario World, Ending screen
- Web IDE screenshots courtesy of their respective sites.