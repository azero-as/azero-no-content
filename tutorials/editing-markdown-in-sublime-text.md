# Editing Markdown in Sublime Text

**If you are new to Sublime you might want to try out [Atom](https://atom.io/) as it built in live preview support of Markdown(All you need to do is press `ctrl+shift+m`)**

Editing Markdown without previewing it from time to time can be frustrating. We will therefore look at how we can set up sublime with markdown and a preview.

There are sublime packages that suports live preview but at the time of writing(2017.08.06) I could not find a working settup that worked with little effort. So this guide explaines how to get a preview with running a command when previewing.

This guide shows how a setup with [GitHub Flavored Markdown (GFM)](https://github.github.com/gfm/). It is however possible to chose plain Markdown in each step.

1. Install packages in Sublime with [Sublime Text Package Control](https://packagecontrol.io/installation)
    1. Copy the text and copy it
    2. Open sublime
    3. Go to `View` -> `Show Console`
    4. Paste the text into the console and pres enter
    5. Press `ctrl+shift+p` to open `Command Palette`
    6. Start writing `Package Control:
    7. Select `Package Control: Install package` and press enter
    8. Start typing the name of the package you want to install

 2. Install the package `Markdown Editing` and `Markdown Preview`

 3. Open the file you want to edit and then the `Command Palette` and enter `set syntax: markdown GFM` (if you want GitHub flavored markdown).

 4. Open `Command Palette` and enter `Markdown Preview: Preview in Browser` and select `github` (if you want GitHub flavored markdown). This opens a new browser window. To reload hit run it again.


This guide is based on [Cheng's Blog - Sublime Text 3 Markdown](http://cheng.logdown.com/posts/2015/06/30/sublime-text-3-markdown)
