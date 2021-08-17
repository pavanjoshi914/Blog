---
title: "GSoC Coding Period - Week8 and Week9 Report"
last_modified_at: 2021-08-17T16:20:02-05:00
categories:
- GSoC
tags:
- GSoC
---
 
![i18n-gsoc-cover]({{ site.url }}{{ site.baseurl }}/assets/images/gsoc/i18n_gsoc_cover.png)
 
After finishing my work on the ```Rails``` and ```JavaScript``` codebase, I started my work with CircuitVerse Mobile App written in ```Flutter```.
 
> **Flutter is widely used and popular Open Source Software Development tool and It is used to develop cross platform applications for Android, iOS, linux etc.**
 
Despites of some of the benefits, such as rapid mobile app development, Flutter was quite in discussion for its uneasiness for internationalization (I18n). 
 
Major I18n packages provided by ```Dart community``` were the ```intl``` and ```flutter_localizations``` package. Their previous configuration of I18n uses a complex approach to feed translations in the app and needs to be upgraded to a cleaner workflow.
 
Here is the glance of previous I18n workflow provided 👀
 
This requires CLI commands to generate localization class generation and needs to follow the steps given below -
 
* Create string resources for all the strings present in app
* Create AppLocalizations class and AppLocalizationsDelegate
* Generate ```.arb``` files from string resources
* Convert them into dart code by creating ```messages_all.dart``
* Translations can be feed using ```AppLocalizations.of(context).title```
 
This was updated to more cleaner workflow as follows -
 
Upgraded workflow will provide easy steps to provide optimal I18n support in Flutter and considered to be used 🔽
 
* Add ```intl``` package and ```flutter_localizations``` package with flag generate:true
* Create ```l10n.yaml``` describing path of translation directory and name of localization class.
* Add localization delegates to the flutter main.dart
* Create ```.arb``` files for providing translations.
* Run ```flutter packages``` to trigger automated localization class generation.
* Use ```AppLocalizations.of(context).key_name``` to provide translation.
 
Upgraded workflow provides automated localization class generation and easy workflow to fill translations in existing translation files.

-------------------------------------------------------------------------------------------------------
 
## Week8 - Upgrade I18n Workflow and Begin Working with Mobile App 🔄
 
Mobile App interface in Flutter is basically made of a number of built in widgets and custom widgets
 
1. Built in widgets provided Flutter API for rapid App Development
2. Custom Widgets created by Developers for specific purposes
 
Following tasks were achieved during this week ⏬ 
 
* Upgrade I18n workflow with the more appropriate one
* Localize built in widgets using flutter_localizations package(package supports 80 different locales)
* Localize Custom Widgets(UI of Flutter) using Intl package
 
## Week9 - Continue Localizing Custom Widgets 💻 
 
As most of the Flutter UI is made of Custom Widgets, corresponding sections took ample amount of time for doing I18n in them.
 
Flutter uses the concept of companion messages for interpolation, and hence I had to use companion messages wherever Interpolation was needed.
 
Companion messages generally convert localization key names into methods and hence we can pass variables as an argument so that there is no need of breaking string.
 
Along with this I had to find solutions for the unit tests, unit tests for localized Flutter widgets needs delegates and current locale to be defined explicitly.
 
Following tasks were achieved during this week ⏬ 
 
* Create a Language Switcher using the locale provider package.
* Continue localization in Custom Widgets
* Fix unit tests for all the Custom Widgets
 
 -------------------------------------------------------------------------------------------------------
 
*A major problem here is we can't use the I18n function outside the ```BuildContext``` i.e I18n will work fine in widgets but not outside the widgets. App also contains models, services and constants which need to be localized.*
 
Currently I am trying to find the solution for the same. ☑️
 
For more, stay connected!!
 
Best Regards ~ Pavan
