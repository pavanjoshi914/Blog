---
title: "GSoC Coding Period - Week1 + Week2 Report"
last_modified_at: 2021-06-25T16:17:02-05:00
categories:
 - GSoC
tags:
 - GSoC
---

Hey folks! :wave: GSOC coding period was officially started on 7 June :man_technologist: :man_technologist:. After the community bonding period this is my first article on coding period, sharing my first two weeks coding period experience with CircuitVerse. 

## My Project Details 📋 

> **_Internationalization mainly aims at creating I18n architecture for the different platforms in order to localize or translate them in multiple languages._**

In short, my aim during GSoC is to make ***CircuitVerse*** platform a ***Global Platform*** so that it can be introduced at global level. It will help both Indian as well as foriegn clients to use it efficiently and make the most out of it.

During GSoC I will be creating ***I18n architecture*** for ***5 major technologies*** used in different CircuitVerse platforms. <br>

:one: Rails (CV main platform) <br>
:two: JavaScript (CV simulator) <br>
:three: Jekyll (CV interactive book) <br>
:four: Flutter (CV mobile app)<br>
:five: DocsifyJs (CV docs)<br>

---------------------------------------------------------------------------------------------------------------

## Week 1: Turning Coffee into Code (☕ - 💻)

In this week, I started setting up fresh repositories for ***Rails codebase*** along with ***linters*** and my favourite extension ```RuboCop``` for Rails.

Prior to the coding period, the complete project was divided into multiple tasks. Among them, following tasks were acheived during Week 1. 

1. <strong>Adding locale to CircuitVerse API endpoint </strong>

      * CircuitVerse API exports ruby objects in form of JSON via data serialization techniques using ```FastJsonapi```. Mobile app renders such data to show content of main platform in mobile app.

      * Adding locale value and updating JSON Schema of User API will help in using same locale value used by user in main platform in mobile app also.

2. <strong>Using ISO standards for locale on frontend</strong>

      * Next task was to convert locale acronymns into full names following ```ISO 639-1 standard language codes```. and integrating them with CV forms. This is helpful in picking up desired language almost instantly.

3. <strong> Initial I18n setup in Rails</strong>

      *  Basic I18n setup to make use of nested directory structure
      *  Fixing rspec test to adapt new changes and updating JSON schema for users as well as project API.
      *  Other relevant tasks including prepation of yml directory structure, translating page in alternate locale, etc.

My first PR was merged with the awesome feedback by mentors 🤩 

![search by category]({{ site.url }}{{ site.baseurl }}/assets/images/gsoc/post4/feedback.png)


During this week, I also had a call with my mentors for discussing I18n architecture for Simulator.

## Week 2: Begin with Localizing CV Modules ⏬

1. <strong> Preparing localization Rules </strong>

      * 2nd week started with preparing bunch of localization rules for CV Rails platform and document them so that consistency in I18n is maintained throughout the codebase by myself as well as by future contributors.

      * This includes designing module specific rules by having proper overview of codebase.

2. <strong> Introducing first I18n architecture for Simulator </strong>

    * I decided to go with famous ```i18n-js``` library for giving I18n architecture to Simulator. Integration worked great in perspective of I18n but failed in terms of dependency on Rails.

    * I18n-js is present in form of gem as well as npm library but module they are using are still written in ruby and requires erb loader with webpacker for its integration.

    * CV simulator needs backend independent architecture so that it can be decoupled in future and integrated in other platforms such as mobile app.

      Currently, I am working further and doing more research on proper backend independent JS libarary for Simulator.

3. <strong>Localization of CV Modules</strong>

    * Week 2 was the beginning of localizing 23 modules. Out of which 10 modules where localized in 2nd week.

    * Pushing a bunch of changes in single PR is irrelevant and also hard to review for mentors. Regarding this, I decided to create different PR for each module. Hence a proper workflow of 2 PR's was created for review and merge at a time.


**Some of the aspects where more care is to be taken while doing I18n in modules were**  🔷
    
  1. Use of proper designed module specific rules.
  2. Taking care that logic doesn't break while introducing I18n
  3. Use of powerful features of Rails I18n API.
  4. Directory Structure
  5. Key-value pair naming conventions along with interpolation and pluralization.

------------------------------------------------------------------------------------------------------------------------

## What I learned 🎯

* More exposure to API and data serialization
* Creation of localization rules to give best possible infrastructure.
* Working with RSpec tests and behaviour driven development
* Experience of integrating different JavaScript libraries
* Designing backend independent I18n solutions.
* Core knowledge of I18n and about localization of modules

For more, stay connected!!

Best Regards ~ Pavan
