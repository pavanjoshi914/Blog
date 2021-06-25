---
title: "GSoC Coding Period - Week1 + Week2 Report"
last_modified_at: 2021-06-25T16:17:02-05:00
categories:
 - GSoC
tags:
 - GSoC
---

After the comunity bonding period , GSoC coding period was officialy started on June 7. In this post I am sharing my experience during first two weeks of coding period with CircuitVerse.

## Details about my Project

Internationalization mainly aims as creating proper I18n architecture for the platforms in order to localize or translate platform in mulitple languages.

In short my aim during GSoC is to make CircuitVerse platform a global platform so that platform can be introduced at global level and Indian as well as Foreign clients can make most out of it.

During GSoC I will be creating I18n architecture for major 5 technologies used in different CircuitVerse platforms
1. Rails (CV main platform)
2. JavaScript (CV simulator)
3. Jekyll (CV interactive book)
4. Flutter (CV mobile app)
5. DocsifyJs (CV docs)

## WEEK1 - Turning coffee into code

During week1 I started with setting up fresh repositories for Rails codebase along with linters and my favourite extension ```RuboCop``` for Rails.

According to the tasks for the project divided prior the coding period following tasks were achieved during week1.

1. Adding locale to CircuitVerse API endpoint

   CircuitVerse API exports ruby objects in form of JSON via data serialization techniques using ```FastJsonapi```. Mobile app renders such data to show content of main platform in mobile app.

   Adding locale value and updating JSON Schema of User API will help in using same locale value used by user in main platform in mobile app also.

2. Using ISO standards for locale on frontend

    Next task was converting locale acronymns into full names following ```ISO 639-1 standard language codes.``` and integrate them with CV forms. This is helpfull in picking up desired language almost instantly

3. Initial I18n setup in Rails

    1. basic I18n setup to make use of nested directory structure
    2. fixing rspec test to adapt new changes, updating JSON schema for users as well as project api.
    3. other relevant tasks including prepation of yml directory structure, translating page in alternate locale etc.

My first PR was merged with the awesome feedback by mentors

![search by category]({{ site.url }}{{ site.baseurl }}/assets/images/gsoc/post4/feedback.png)

During week1 I also had a call with my mentors discussing I18n architecture for Simulator.

## Week2 - Begin with localizing CV modules

1. Preparing localization Rules

    Week 2 started with preparaing bunch of localization rules for CV Rails platform and document them so that consistency in I18n is maintained throughout the codebase by myslef as well as by future contributors.

    This includes designing module specific rules by having proper overview of codebase.

2. Introducing first I18n architecture for Simulator

    I decided to go with famous ```i18n-js``` library for giving I18n architecture to Simulator. Integration   worked great in perspective of I18n but failed in terms of dependency on Rails.

    i18n-js is present in form of gem as well as npm library but module they use are still written in ruby and requires erb loader with webpacker for its integration.

    CV simulator needs backend independent architecture so that it can be decoupled in future and integrated in other platforms such as mobile app.

    Work in Progress!!, currently doing more research on proper backend independent JS libarary for Simualator

3. Localization of CV Modules

    Pushing bunch of changes in PR is irrelevant and hard to reivew for mentors as well. regarding this I decided to create different PR for each module. Hence a proper workflow of 2 PR at a time for review and merge was created.

    Week2 was the begining of localizing 23 modules outof which 6 modules where localized by me. This includes

    1. introducing translation function in ERB templates.
    2. Creating proper translation directory structure according to localization rules.
    3. Proper Naming conventions according to localizationr rules.


## What I learned

1. More exposure to API and data serialization
2. Creation of localization rules to give best possible infrastracture
3. Working with RSpec tests and behaviour driven development
4. Experience of integrating different JavaScript libraries
5. Designing backend independent I18n solutions.
5. Core knowledge of I18n and about localization of modules