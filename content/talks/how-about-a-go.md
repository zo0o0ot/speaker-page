---
title: 'How About a Go?'
date: "2018-08-06T14:30:00-05:00"
url: "/talks/how-about-a-go/"
event: "That Conference 2018"
location: "Kalahari - Wisconsin Dells, WI"
site: "https://github.com/zo0o0ot/how-about-a-go"
video: "https://youtu.be/XdnU4GbZoW8"
slides: ""
thumbnail: "/talks/images/that18.png"
image: "/talks/images/present-notes.png"
description: "An introduction to Golang from a beginner's perspective."
---

Go: A beginner’s perspective. What's the Google Go language (Golang) really good for? Is it “worth a go”? Ease of deployment, simple syntax, and native concurrency make for strong arguments! You will hear about Go from a beginner's point of view.

No Go experience is necessary.  

You will learn more about Go, and leave with a better idea of whether Go is a language that you should learn and use in either personal or business projects. I will also give suggestions for five “first projects” for people new to Go.

Here is a photo of the session from the [THAT Conference 2018 Flickr album](https://www.flickr.com/photos/thatconference/albums/72157694062985220).

![Picture of 2018 session](/img/confs/2018_that_speaking_01.jpg)


Although the talk itself was not recorded, I did do an interview with Clark Sell about Golang at That Conference, and the video of that conversation is linked to the talk here.

[![The Go gopher](/img/go-gopher.gif)](https://golang.org/)

*One issue with providing this presentation after the fact is that it was written in golang, using the [go present tool](https://halyph.com/blog/2015/05/18/golang-presentation-tool.html), which allowed me to run code snippets live during the presentation. However, the attempts that I've made to export it to a more portable format like PDF have all failed.*

If you'd like to see the actual code that I ran and the markdown for the slides with presenter notes, they are [available in GitHub](https://github.com/zo0o0ot/how-about-a-go).

Golang is cross-platform, so on Windows/Mac/Linux, you can install golang and the present tool to run the presentation yourself. If you have go and present installed, you can clone [this repository](https://github.com/zo0o0ot/how-about-a-go) and run present in the root directory of the project to see the presentation locally in your browser (likely at 127.0.0.1:3999). Run present -notes and press "n" in the browser to see the presentation notes open up in a separate browser tab.

In case you're not in the mood to do that, the raw markdown for the presentation is below:

```markdown

# http://godoc.org/golang.org/x/tools/present
# Present files have the following format. 
# The first non-blank non-comment line is the title.
# The subtitle, date, and tags lines are optional.
How about a Go?
That Conference
6 Aug 2018
Tags: golang, ThatConference, projects
: Welcome to my session.


Ross Larson
Software Developer, WTS Paradigm
rosslarson@gmail.com
http://about.me/rosslarson
@rosslarsonWI
: GitHub repo for this presentation - https://github.com/zo0o0ot/how-about-a-go

* 
.background images/ThatBranding.png
: We're at That Conference!

* 
.background images/ThoseSponsors.png
: Thanks to the sponsors.  You make it happen.

* Agenda
- The History of Golang
- Projects that use Golang
- General language overview
.code code/go-vision/vision.go /^func sample/,/^}/
- Pros and Cons of Golang
- Tools to code with Go
- Project suggestions
: As a note, there is going to be some code on slides in my session.  I am unable to change the size of the font, so you may wish to sit closer than usual for this session.  I'll wait if you want to move up.
: I have a screen magnifier that could be used if it's a real emergency.
: We are going over some stuff here.  It is going to be awesome.

* History of Golang
.background images/Go-Logo_Blue.svg
: There is some history here, even though the language is relatively young.  It started at Google in 2007.
: The authors of Go noticed several trends in the last 10 years or so that Systems Languages were not easily able to take advantage of.
: Computers are enormously quicker but software development is not faster.
: Multi-core systems are more common, but it is difficult to write software that takes advantage of the additional resources.
: Some fundamental concepts such as garbage collection and parallel computation are not well supported by popular systems languages.

* Creators of Golang
- Ken Thompson (B, C, UTF-8, Unix)
- Rob Pike (UTF-8, Plan 9)
- Robert Griesemer (Java Hotspot VM, Google V8 JS engine)
.image images/RobertRobAndKen.jpg
: The three main inventors of were three Engineers that were working at Google (after having done some pretty impressive things in their past)
: According to Ken Thompson, here's what happened "When the three of us [Thompson, Rob Pike, and Robert Griesemer] got started, it was pure research. The three of us got together and decided that we hated C++. [laughter] ... [Returning to Go,] we started off with the idea that all three of us had to be talked into every feature in the language, so there was no extraneous garbage put into the language for any reason."
: They started working on the language internally in 2007, open sourced the language in 2009, and released version 1 of Golang in 2012.  The current version of Go is 1.10, and 1.11 is due to come out in August. Releases seem to come out every six months or so.
: 1.11 draft release notes - https://tip.golang.org/doc/go1.11

* The Go Gopher
.background images/blue-background.jpg
.image images/gopher.svg
: The Go Gopher was introduced when Golang was open sourced in 2009. It was designed by Renee French. https://blog.golang.org/gopher

* Projects that use Golang
- Docker
- Kubernetes
- YouTube
- Uber
- Cloudflare
- Hugo
.background images/Go-Logo_Blue.svg
: Despite the goofy gopher, this is a language that can solve some serious problems.  Some impressive projects use this language, with Docker probably being one of the most popular examples.
: Hugo was what got me interested in Golang.
: Go project wiki -https://github.com/golang/go/wiki/Projects

* General language overview
.background images/Go-Logo_Blue.svg
: Enough talk, let's look at some code.

* Hello World
.play -edit code/hello/hello-world.go
: Here's some go code. It contains a package, import statements, and a main function.  Note the native support of UTF-8.

* Variables and Types
.play code/types/data-types.go
: Here's some variables and data types. There are a few of them. bool, string, int, int8, int16, int32, int64, uint, uint8, uint16, uint32, uint64, uintptr, byte, rune, float32, float64, complex64, complex128
: Rune is an int32 code point.  It's got something to do with how Go handles UTF-8 characters. For more info on strings and characters - https://blog.golang.org/strings
: unitptr is an integer type that is large enough to hold the bit pattern of any pointer. https://golang.org/pkg/builtin/#uintptr

* Functions and Return Values
.play code/multiple-returns/multiple-returns.go
: Functions are a thing.  They start with func. They can return nothing, one value, or multiple values.

* If, Else, and Switch
.play -edit code/if-else-switch/if-else-switch.go /^func itsNine/,/^}/
: If, Else, and Switch statements work like most other languages.  The parentheses are not required, but the braces are. One note - There is no ternary if (?:) in Go. You have to write out the whole if statement.
: In Go, you can initialize a variable inside the if statement before you check it.  If you do it that way, the variable is scoped to the if statement.
: Switch statements exist, too.  They seemed to work how I expected them to work.

* For loops
.play -edit code/for-loops/for-loops.go /^func theCount/,/^}/
: For loops are pretty versatile in Go. The syntax goes "for declaration;condition;incrementer".  However, you can omit some or all of these arguments.
: Therefore, for is also Go's while.  Be careful for infinite loops! I made at least one while creating this sample code.

* Arrays
.play code/arrays/arrays.go /^func arraysDemo/,/^}/
: In go, arrays are slightly more limited than in other languages.  Once they have been created, their length cannot be changed.  Nothing can be appended to them, but the values inside of the array can be changed. You can also refer to the range inside of an array like [x:y], but you have to note that the array position in the beginning of the array is included, but the array position at the end gives you everything UNTIL that array position, NOT INCLUDING the given number.  You can also omit the number to go to either the upper or lower limit.
: When referring to arrays in a for loop, you can do the rough equivalent of a foreach loop by using range. It returns two values - the location in the array, followed by the contents.

* Slices
.play code/slices/slices.go /^func slicesDemo/,/^}/
: Slices are a more flexible alternative to arrays. You can append to them, as well as copy them. They are zero indexed, like arrays.  When you want to refer to them, the variable gives you the whole object, or you can specify a range.  Range works similar to arrays.
: Note that there is not an easy way to remove from the middle of a slice - Link to slice tricks https://github.com/golang/go/wiki/SliceTricks

* Maps
.play code/maps/maps.go /^func showSomeMaps/,/^}/
: Maps are a key value store.  They are similar to slices, but you can name the keys instead of needing to use numbers.  They are like dictionaries in python and HashMaps in C#. Maps do not store these key/value pairs in any particular order, so if you print out the whole map, the order of the keys will vary.

* Pointers
.play code/pointers/pointers.go
: Pointers are a thing in go. They point to another variable in memory. They can even point to another pointer. Garbage collection of pointers is automatic.
: References exist in Go, as well. Pointers are more powerful and flexible, and appear to be used more often in Go code. I believe it has to do with being able to reassign a pointer, but not a reference. There's an article that explains the difference. http://spf13.com/post/go-pointers-vs-references/

* Structs
.play code/structs/structs.go
: A struct is a collection of fields.  It can also have methods.
: Q- Is Go Object Oriented? `Yes and no. Although Go has types and methods and allows an object-oriented style of programming, there is no type hierarchy. The concept of “interface” in Go provides a different approach that we believe is easy to use and in some ways more general. There are also ways to embed types in other types to provide something analogous—but not identical—to subclassing. Moreover, methods in Go are more general than in C++ or Java: they can be defined for any sort of data, even built-in types such as plain, “unboxed” integers. They are not restricted to structs (classes). `
: Comparing structs to objects. https://golangbot.com/structs-instead-of-classes/

* Errors and nil
.play code/error-creating/error-creating.go
: You may have noticed that go functions allow multiple return items.  Go takes full advantage of this for its error handling system. Most functions return an error all of the time, assigning it to "nil", which is equivalent to null.  When the error does exist, you can handle the error appropriately. You can create your own error message which includes customizable information.
: Go error documentation - https://golang.org/pkg/errors/ and https://golang.org/doc/effective_go.html#errors

* Fancy Errors!
.play code/fancy-error/fancy-error.go /START OMIT/,/END OMIT/
: In addition to customizing the error string, you can also return other relevant information. You can return a struct in the error.

* Errors at Compilation
.play -edit code/compilation-error/compilation-error.go
: Go is relatively picky when it compiles.  It would prefer to tell you about problems as you compile your code as opposed to when you execute your code.

* Interfaces
.code code/interface/interface.go /^type geometry/,/^}/
.code code/interface/interface.go /^type rect/,/^}/
.code code/interface/interface.go /^type circle/,/^}/
: Interfaces are named collections of method signatures. Basically, you indicate what it returns, and the interface doesn't really care how you do it.
: Links - Golang Interfaces Explained - https://youtu.be/F4wUrj6pmSI 
: Effective Go- Interfaces - https://golang.org/doc/effective_go.html#interfaces_and_types
: More explanation of Interfaces - https://medium.com/golangspec/interfaces-in-go-part-i-4ae53a97479c

* Interfaces, Part 2
.code code/interface/interface.go /START OMIT/,/END OMIT/

* Interfaces, Part 3
.code code/interface/interface.go /^func measure/,/^}/
.play code/interface/interface.go /^func main/,/^}/

* Concurrency
.play -edit code/goroutines/goroutines.go
: Concurrency allows for a program to be split into manageable chunks that can be executed separately and efficiently.
: A goroutine is a lightweight thread managed by the Go runtime.
: There is also something called a channel which allows goroutines to communicate with each other, but explaining that tends to get into the weeds quickly.
: Links -  https://www.golang-book.com/books/intro/10   Probably need to explain routines as well- https://tour.golang.org/concurrency/1
: Concurrency in Go video- https://youtu.be/LvgVSSpwND8

* Testing
- woo.go
.play code/builtin-testing/woo.go /^func Woo/,/^}/
- woo_test.go
.code code/builtin-testing/woo_test.go
: Testing is built into go. If you create a file with the same name and append "_test" to the file, it can automatically run the tests. Test functions have the word test before them. For more info - https://golang.org/pkg/testing/ 
: (Open woo_test in VS Code to show tests.)
: The Go compiler and linker will not ship your test files in any binaries it produces.

* Debugging with Delve
.background images/blue-background.jpg
.image images/delve.png _ 900
: Go has a tool called delve that helps with debugging of your go code. https://github.com/derekparker/delve
: You can use it on the command line with `dlv debug`. There are also plugins for most Go editors. https://github.com/derekparker/delve/blob/master/Documentation/EditorIntegration.md
: Delve supports both local and remote debugging.
: I'm going to show off the "slices" code in Visual Studio Code with the Delve Plugin. Note- there is currently a bug where VS Code force quits delve before it can clean up debug files.  They are working on fixing that soon.  https://github.com/Microsoft/vscode-go/issues/1797

* Pros and Cons of Golang
.background images/Go-Logo_Blue.svg

* Pros
.background images/blue-background.jpg
.image images/go-gopher.gif
: Let's start with the Pros.  This may be highly subjective.

* Golang Pros
- Simplicity
- Automatic code formatting with gofmt()
- "Idiomatic Go"
- Relatively simple Concurrency
- Built-in webserver
- Quick Performance
- Garbage Collection
- Integrated Testing and Benchmarking
: Go was not designed to be a "kitchen sink" language. One of the stated goals was to produce straightforward, readable code.
: Golang has clearly defined standards and formatting suggestions.  There's even a command called `gofmt()` that will format your code the "correct" way.  Many golang editors will do this automatically as you save the file.
: The language was designed to have "one correct way" of doing things, which is referred to as "Idiomatic Go". One of the stated goals was to make legacy code easier to read and maintain.
: Links - https://golang.org/doc/effective_go.html ---https://github.com/golang/go/wiki/CodeReviewComments

* Golang Cons
- Simplicity
- Unclear niche
- Libraries and support are still a work in progress
- "Idiomatic Go" and the Somewhat opinionated community
- Dependency management is still somewhat new
- Not object oriented in the traditional sense
: It's not all sunshine and rainbows here. Though the standard libraries are quite good, third party libraries may not be to the same quality and quantity that you are used to with other languages.
: A drawback to the "Idiomatic Go" concept is that since there is one "best" way to do many things in Go, you may run into a lot of people who will tell you that you're doing it wrong.  Also, the Golang Slack team was a firehose of information, and when I asked a question there, it was completely ignored.
: Go dep (the official dependency management tool) is still in "experimental form".  See https://golang.github.io/dep/ --- Go 1.11 adds preliminary support for a new concept called “modules,” an alternative to GOPATH with integrated support for versioning and package distribution. It's exciting, but coming from other languages, you may be expecting a more mature set of tools to manage dependencies and packages.

* Tools of the Trade
.background images/Go-Logo_Blue.svg
: There are a few options for Go development.  I've been doing most of my coding with Visual Studio Code and the associated golang plugins. https://code.visualstudio.com/docs/languages/go  Atom has similar extensions, but VS Code seemed to work for my needs.
: I gave GoLand, the JetBrains Go IDE, a try.  It seemed nice, but it may be a little heavier than I needed as a beginning dev.  It's possible that it does some things better, such as finding references to functions or refactoring. https://www.jetbrains.com/go/
: LiteIDE is a cross-platform editor for Go that's under development.  One thing that is nice about it is that it does syntax highlighting of Go's slide format. I used it for that. https://github.com/visualfc/liteide
: Official wiki of Go Editors and IDEs: https://github.com/golang/go/wiki/IDEsAndTextEditorPlugins

* Suggested Projects
.background images/Go-Logo_Blue.svg
: Enough theory.  Let's do some projects.

* Make a presentation with Go Present!
- This presentation is an example!
.image images/present-notes.png
: This presentation was made using Go's present tool.
: I made the presentation (including notes) in a modified version of Markdown, and Go's present tool creates a web server that serves up webpages on my machine that I access via a browser.
: There's a fancy thing that it also does with websockets to allow me to run code from the browser and display the results.  It's cool.
: For more info - https://talks.golang.org/2012/insidepresent.slide#1

* Do some web scraping with Colly!
.image images/colly.png
: Colly is a tool (written in Go) that allows you to scrape web pages programmatically in Go.
: Link to site - http://go-colly.org/

* Create a static website with Hugo!
.image images/gohugo.png
: Hugo is an excellent static site generator.  I found out about it last year during "The Static Web Revolution" presentation by Steven Hicks at That Conference (https://old.thatconference.com/sessions/session/11195).

* Create a Slack Bot!
.image images/slack.png _ 900
: You can use Go to create your own Slack Bot!
: Link - https://www.opsdash.com/blog/slack-bot-in-golang.html
: Another link - https://medium.com/mercari-engineering/writing-an-interactive-message-bot-for-slack-in-golang-6337d04f36b9

* Run Go in the Cloud, or in the Browser!
.image images/clark-vision-api.png
: Google Compute Platform (GCP) and AWS Lamda both support Go. (https://cloud.google.com/go/home) (https://aws.amazon.com/blogs/compute/announcing-go-support-for-aws-lambda/) --- Also nearly every cloud platform has an SDK for Go to use for management of cloud resources.
: I was able to create a Vision API label retriever in about 5 minutes on Google Cloud Platform, but a variety of other APIs were available, as well. Code is available in the repo for this presentation, but you'll have to create your own compute instance.
: Also, Golang 1.11 supports WebAssembly as a target, so if you're looking to run Go code in the browser, that's in the process of happening.
: Five projects not enough?  Try one a week for a year! https://github.com/kkdai/project52

* Questions?
.background images/Go-Logo_Blue.svg

* 
.background images/ThatConference2019.png
: See you next year!

* Resources for learning Go
- A Tour of Go
- Go By Example
- Effective Go
- Go Wiki: Code Review Comments 
- Pluralsight / Lynda courses

*** YouTube tutorials and presentations
- Rob Pike
- Steve Francia
- Francesc Campoy (Just For Func)

: There are both free and paid resources for learning Go. I focused a lot of my learning on the Tour of Go (https://tour.golang.org/list) and Go By Example (https://gobyexample.com/).  Free resources can get you pretty far.
: More advanced free resources are Effective Go (https://golang.org/doc/effective_go.html) and Go Code Review Comments (https://github.com/golang/go/wiki/CodeReviewComments)
: 7 Common Mistakes in Go - Steve Francia - https://youtu.be/29LLRKIL_TI
: Go proverbs - http://go-proverbs.github.io/
: Go on Pluralsight - https://www.pluralsight.com/courses/go and on Lynda - https://www.lynda.com/Go-training-tutorials/7052-0.html
```