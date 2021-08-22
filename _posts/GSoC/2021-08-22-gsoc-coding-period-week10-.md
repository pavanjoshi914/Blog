---
title: "GSoC Coding Period - Week10 Report"
last_modified_at: 2021-08-22T16:20:02-05:00
categories:
- GSoC
tags:
- GSoC
---
 
![gsoc-final-cover]({{ site.url }}{{ site.baseurl }}/assets/images/gsoc/post10/i18n_gsoc_cover.png)

Today marks the end of my 10-week programming journey at CircuitVerse under Google Summer of Code.🥳

> ***All the code served to community, initial reviews, improvements in existing code, blogging, weekly catchup calls with mentors and team members felt awesome!!***

This blog post summarizes my work done in last week of GSoC coding period.

As I have already finished my working in major 3 platforms i.e. Main Platform, Simulator, and Flutter Mobile App, it was the time to work on DocsifyJS and do relevant improvements in the previous work.

## Mechanism behind I18n for DocsifyJS

 DoscifyJS is simple JavaScript framework, when loaded into HTML file gives theming facility to the documentation. Such project structures can be simply served using Python Simple HTTP servers.

As it is a very simple structure, it is a very good practice to design general i18n mechanism without using any external tool.

For this, three tasks need to be done :-

 1️⃣ Load NavBar and SideBar dynamically according to the language.
 
 2️⃣ Mechanism so that language switcher works well.

 3️⃣ Load content(Markdown) dynamically in the DOM of web page accoring to the current active language.

All the above tasks can be performed simply using basic logic to workaround the concept of generating links for each file.

![i18n-gsoc-cover]({{ site.url }}{{ site.baseurl }}/assets/images/gsoc/post10/docsify.png)

-------------------------------------------------------------------------------------------------------

## Week 10: I18n Architecture in DocsifyJS and Final Enhancements ✨

Following tasks were achieved during this week ⏬

* I18n in DocsifyJS via a designing mechanism for loading sidebar, navbar, and markdown dynamically into the Page.
* Language Switcher for DocsifyJS
* Fixes in Rspec tests and enhancing Language switcher for Rails and Simulator capable of handling scenarios such as -

  1. Language switching when the user is not logged in(session-based).
  2. Language switching when the user is logged in.
  3. Taking care that, language switching through switcher and user form should not conflict with each other.

  ### Implementation 🔄

* [I18n in CircuitVerse Main Platform (3000 lines of code)](https://github.com/CircuitVerse/CircuitVerse/pull/2397)
* [I18n in CircuitVerse Simulator (1100 lins of code)](https://github.com/CircuitVerse/CircuitVerse/pull/2368)
* [I18n in CircuitVerse Mobile App (2500 lines of code)](https://github.com/CircuitVerse/mobile-app/pull/126)
* [I18n in CircuitVerse Docs (excluding markdown content - 100+ lines of code)](https://github.com/CircuitVerse/CircuitVerseDocs/pull/307)

&nbsp;

-------------------------------------------------------------------------------------------------------

### Major MileStones Achieved  ☑️

* Complete Infrastructure for Internationalization of Rails Platform.
* Complete Infrastructure for Internationalization of Simulator Platform.
* Complete Infrastructure for Internationalization of Mobile-App.
* Complete Infrastructure for Internationalization of CircuitVerse-Docs.

I felt amazing after completing my work on the different technologies and codebases during this journey! 🥳 

## Final Evaluations 📧

In the upcoming days, mentors will be reviewing my code and will be uploading my results on GSoC portal. Lets hope for the best🤞!! 

For more, stay connected!!
 
Best Regards ~ Pavan

