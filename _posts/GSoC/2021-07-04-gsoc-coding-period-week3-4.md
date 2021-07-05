---
title: "GSoC Coding Period - Week3 + Week4 Report"
last_modified_at: 2021-07-04T16:17:02-05:00
categories:
- GSoC
tags:
- GSoC
---
 
Hey Readers!👋 The first two weeks of coding period was a great learning experience for me, along with positive feedbacks by mentors on my pull requests.🤩😎 
 
> _**In that duration, I created the I18n infrastructure for the first 10 CV modules along with some parallel coding work and experimentations.**_ 🏁

----------------------------------------------------------------------------------------------------------------
 
## Week 3: Working with CV Modules - Ruby Gems - Mailers 💻 
 
It was the beginning of completing my work on the remaining major modules. Some of the modules like ```logix``` took 500 lines of code changes.
 
It was quite hard to understand and get familiar with part of codebase I haven't visited before. Unfamiliar modules took an ample amount of time in understanding Ruby code and JavaScript based logic along with running quality I18n processes on them.
 
 1. <strong>Working with modules</strong>

      *  This week I completed my work in 6 major modules along with provisional completion of the remaining 7 modules.
      *  Testing and experimentation will be carried in upcoming weeks before the final deployment to the CircuitVerse Servers.
 
 2. <strong>Working with gems</strong>
 
       * I also had a strong hand on understanding the structure of different gems such as ***devise***, ***activerecord error messages***, ***commentator***, ***activity notifications***, ***mailers***, ***paginators*** etc.
       * I also got introduced with the awesome gem ```MailCatcher``` which can catch mails send locally and can show us direct results.
 
At the end of this week, I finally completed my major work on all 23 modules which is a single modules on its own 💠 3 PRs merged and current two under review.
 
 ----------------------------------------------------------------------------------------------------------------------------------------------------------------------
 
## Week 4: ```banana-I18n``` Integration - Other Modules ⏬
 
During this week, I felt relaxed as major work required was already done locally. I started working on ```banana-I18n``` JavaScript library along with working on controllers, helpers etc on Rails side.
 
Before ```banana-I18n``` I proposed two integrations of ```i18n-js``` in different ways. Second integration still landed with dependency of Rails ***I18n mapping*** 😶😶.

1. <strong>Working with ```banana-I18n``` library </strong>

      *  ```banana-I18n``` library is a Pure JavaScript form of Jquery-I18n library developed by wikipedia. They also provide React and Vue bindings of the library for use in specific environments.
 
      *  In our case JavaScript modules are statically compiled by ```webpacker``` and are served on frontend. As ```banana-i18n``` is written purely in JavaScript it was a good choice at first glance.
 
      *  Basically this library allows us the instantiation of a constructor which can hold an object named ```messages``` which when passed to the constructor, the library interprets it through their scripts and provides I18n support for JS based modules.

    Oops!😬 Library don't provide their own ***Asynchronous mechanism*** to load JSON in the library, Here I had to implement ***loading mechanism*** by myself.
2. <strong>Working with Loading Mechanism </strong>

    Here I tested three Asynchronous loading mechanisms ⤵️
 
    * Use of ```Fetch API``` in Web Environment

    * Keeping configuration in Web Environment and implement ```CommonJs``` methods via ```RequireJs library```

    * Use ```ES6``` or ```CommonJs``` environment provided by webpacker
 
3. <strong>Selecting Loading Mechanism </strong>

    *  First method is a very basic method but uses ```HTTP calls for Asynchronous loading```. This won't play nicely in offline apps hence was eliminated after discussion with mentors.
 
    *  Second method depends on external dependency, consequently I tried to avoid using this method.
 
    *  Third method seemed more promising as dynamic loading is also applicable in ```CommonJs Environment```, however ```ESLint``` yelled at me for my approach frequently.
 
*Finally I decided to go with CommonJs methods to dump JSON files into the library, and basic JavaScript to switch between Default language JSON and Current locale JSON.*
 
*If a JSON for the current locale is not available, I had to load default JSON, which can be done easily using ```try{}.. catch{}``` JavaScript syntax.*
 
Here we can ***instantiate default JSON*** in object directly and use ***```try{}... catch{}```***  for current locale JSON, even if asynchronous loading fails for current locale, object will already have a default json file and library will be good to go in any exceptional case.


--------------------------------------------------------------------------------------------------------------------------

 
## What Next
 
 > ***After the end of the upcoming week, Phase one Evaluations will be held from 12 July onwards. According to GSoC timeline mentors will review code and will pass and fail students after analysing the work they had done till now.***
 
* I have completed almost all the tasks that I had committed before Phase one evaluations.🥳🥳 In the upcoming week I will design a test suite for I18n, language switchers and prepare for my phase one evaluations. ☑️
 
* I will also start working parallely on Mobile App and Simulator as well.◾✍️
 
For more, stay connected!!

Best Regards ~ Pavan
