---
title: "GSoC Coding Period - Week6 and Week7 Report"
last_modified_at: 2021-08-1T16:20:02-05:00
categories:
- GSoC
tags:
- GSoC
---
 
![i18n-gsoc-cover]({{ site.url }}{{ site.baseurl }}/assets/images/gsoc/i18n_gsoc_cover.png)
 
Completing my Ruby on Rails codebase work, I started working with JavaScript coded CircuitVerse Simulator during these two weeks.
 
The simulator is currently integrated into Rails using ```WebPacker gem``` to deliver JavaScript on the frontend and Ruby as well.
 
We cannot use Rails I18n in Simulator as individually it was a node-based (ES6) product. As decoupling of Simulator is going on in parallel, I only had to work on JS files served by WebPacker and not interface of Simulator written in Ruby ERB template
 
The simulator structure is divided as follows:
 
1. Configuration files in simulator/src along with third-party npm packages.
2. Digital Circuit elements in form of modules (General modules, Sequential modules and Testbench modules).
3. Relevant tools like themers, hotkey binders (to run custom shortcuts through the keyboard), and data folder handling project-based scenarios.
 
## Week6 - Localizing Configuration files
 
In total there were 36 configuration files written in JavaScript which I had to check as well as localize without breaking any piece of code.
 
Following tasks were achieved during this week ⏬ :-
 
* I18n in Simulator controls interface in UX.js
* I18n in Simulator Guide in tutorials.js
* I18n in Simulator functionalities such as Verilog, SubCircuits, CombinationalAnalysis etc.
* Completing I18n and testing in all the remaining 36 configuration files and functionalities.
 
 
## Week7 - Localizing Circuit modules and some basic services
 
Following tasks were achieved during this week ⏬ :-
 
Here I worked with element modules, hotkey binders, themers, testbench and sequential circuit element modules
 
* I18n in 50 Circuit modules and a total of 17 sequential circuit element modules and testbench as well.
* I18n in themers and hotkey binders
* I18n in mutable properties of Circuit Elements (If Any)
* I18n in configuration handling Current Project Data
 
However, some problems encountered in themers and hotkey binders are that they render JavaScript object keys directly to represent the corresponding field names that can't be touched as it breaks the back-end package.
 
In the end, I finished working on the Simulator which required 800+ code changes and started working with Flutter based Mobile App.

For more, stay connected!!
 
Best Regards ~ Pavan

