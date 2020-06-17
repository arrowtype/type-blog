# Using DrawBot in VS Code

This post is in preparation for a talk at the 2020 Typographics TypeLab.

## Basics

### What is DrawBot?

- Mac only, because it uses macOS text & graphics APIs
- Python Module
- Also has a standalone app

### What is VS Code?

### Starting a script in DrawBot

- The docs are really good for an introduction, and it this session isn’t meant to be an introduction

- [ ] TODO: make “Hello World” example
- [ ] TODO: make drawbot app version of animation starter

### Ergonomic differences

This is nothing at all against the maintainers of DrawBot – I am very grateful for their work & support on it. However, there are features on which a small project can’t compete with a product like VS Code, backed by Microsoft & a huge open-source community.

- Drawbot doesn’t use usual code syntax highlighting theme, and it’s not super easy to configure.
- Can be tricky to update DrawBot app 
  - Automatic updates don’t work for me (this could be a macOS security thing)
  - Because I can only update by downloading a new installation from the website, my preferences get erased each time. Goodbye, theme edits. :(
  - By contast, VS Code just updates without me doing anything
- Text editing tricks in VS Code: 
  - Multi-selection & editing (e.g. for variable renaming)
  - Multi-line editing
  - Moving lines up & down
- Python linting in VS Code
- Built-in Source Control panel & diffing in VS Code

### Where DrawBot is better

- “Drawing” with numbers is very cool
- Faster preview updates

## How to work with DrawBot in VS Code

## Tips

- This relies on saving new files for previews, so you should adjust the timestamp as needed to overwrite or not overwrite exports as needed
  - A good default is letting timestamps have `year_month_day-hour_minute`. That way, as you generate, you will only be left with a new file for each minute of work.
  - If you are making lots of experimental changes and you aren’t worried about saving computer disk space, add `_seconds` to your timestamp and go nuts!
  - If you *are* worried about disk space (e.g. you are exporting large gif files, etc), maybe just go by the `hour`, and change the file name when you actually want to save a specific version. 
- It’s also useful to version with Git, but that deserves its own workshop
- You will occassionally hit a limit on macOS preview where it will stop opening new files. At this point, you will have to click on one of the Preview windows, and use the shortcut **Option Command W** to close all open windows.

------------------------------------------------------------------

## Links

- "Using Drawbot in an external editor"

## Please do these two things:

1. Check out https://arrowtype.github.io/vf-slnt-test/slnt-ital-tests/index.html, scroll to the bottom, and follow links to the Chromium & WebKit issues to voice your support for the prioritization of fixing the rendering of slnt & ital variable axes.

2. Check out https://github.com/fonttools/fonttools/issues/1994 & let me know if you have experienced the same font-menu issue in other fonts or if you know a solution (but this is probably a macOS issue, so at the very least it would be good to show that many people are having trouble here)