# Doom Cricket Foundry VTT Prototype

Doom Cricket is the game of fantasy cricket, where teams do battle using the rules
of cricket, and the tools of war.  

This is a prototype of the game built in [Foundry VTT](https://foundryvtt.com/), following the very excellent
[System Development Tutorial](https://foundryvtt.wiki/en/development/guides/SD-tutorial)
by Matt Smith.  

I am maintaining notes on development in this repo and publishing them on [my website](www.williambidstrup.com).  


# TODOs  

- Learn about gulp to understand gulpfile.js  
- Follow [this tutorial](https://hackersandslackers.com/extract-data-from-complex-json-python/)
to learn more about the package-lock.json




# Devlog

## System Development Tutorial 01  

Set up repo.  

Clone boilerplate system.

There is a requirement to replace the 'boilerplate' names with target system name.  

I chose to go through each file in detail and make the changes manually.
This step could be improved with some clever use of grep in zsh or bash.   

This command will list all files with certain text string in it ``% grep -r 'boilerplate' .``  

Where do these words occur?  

- gulpfile.js: 0  
- package-lock.json: 1  
- package.json: 2
- template.json: 0  
- system.json: 5  
- en.json: 17 (BOILERPLATE)  
- config.mjs: 12 (BOILERPLATE)  
- templates.mjs: 4  
- actor-sheet.mjs: various  
- item-sheet.mjs: various  
- boilerplate.mjs: various  
- some-lib.css: 0  
- some-lib.min.js: 0  


The important ones are [system.json](https://foundryvtt.wiki/en/development/guides/SD-tutorial/SD03-systemjson) and [template.json](https://foundryvtt.wiki/en/development/guides/SD-tutorial/SD04-templatejson).  

I created a chart of the structure of the system folder [here](https://lucid.app/lucidchart/a383c27e-3956-42d9-ae5d-a5504386cc6e/view?page=0_0#).  



## System Development Tutorial 02-03  

Section 02 is mostly for reading, I took no actions.  

Section 03 is about the system.json file which I inspected deeply.  



# System brainstorm

The forces of Chaos play Kricket.  





# Boilerplate System

This system is a boilerplate system that you can use as a starting point for building your own custom systems. It's similar to Simple World-building, but has examples of creating attributes in code rather than dynamically through the UI.

## Usage

Before installing this system, you should rename any files that have `boilerplate` in their filename to use whatever machine-safe name your system needs, such as `adnd2e` if you were building a system for 2nd edition Advanced Dungeons & Dragons. In addition, you should search through the files for `boilerplate` and `Boilerplate` and do the same for those, replacing them with appropriate names for your system.

## Sheet Layout

This system includes a handful of helper CSS classes to help you lay out your sheets if you're not comfortable diving into CSS fully. Those are:

* `flexcol`: Included by Foundry itself, this lays out the child elements of whatever element you place this on vertically.
* `flexrow`: Included by Foundry itself, this lays out the child elements of whatever element you place this on horizontally.
* `flex-center`: When used on something that's using flexrow or flexcol, this will center the items and text.
* `flex-between`: When used on something that's using flexrow or flexcol, this will attempt to place space between the items. Similar to "justify" in word processors.
* `flex-group-center`: Add a border, padding, and center all items.
* `flex-group-left`: Add a border, padding, and left align all items.
* `flex-group-right`: Add a border, padding, and right align all items.
* `grid`: When combined with the `grid-Ncol` classes, this will lay out child elements in a grid.
* `grid-Ncol`: Replace `N` with any number from 1-12, such as `grid-3col`. When combined with `grid`, this will layout child elements in a grid with a number of columns equal to the number specified.

## Compiling the CSS

This repo includes both CSS for the theme and SCSS source files. If you're new to CSS, it's probably easier to just work in those files directly and delete the SCSS directory. If you're interested in using a CSS preprocessor to add support for nesting, variables, and more, you can run `npm install` in this directory to install the dependencies for the scss compiler. After that, just run `npm run gulp` to compile the SCSS and start a process that watches for new changes.

![image](http://mattsmith.in/images/boilerplate.png)
