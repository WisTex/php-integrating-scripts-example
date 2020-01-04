
# Pis&eacute; - PHP Integrating Scripts Example

#### Version 0.1 (Concepts Only)

Concepts and example code for creating scripts that integrate with other scripts.

*Note: Currently this is conceptual only. Example code will be added.*

## Purpose

To provide a fully commented base of code that can be used to build plugins and modules that can easily integrate into existing PHP and HTML websites.

This example code is not designed to work "out-of-the-box" but rather it is designed as a starting point where you create your own custom code on top of it. 

The developer integrating your module into their script may need to configure settings and update include files if they want integration with their website, although you can provide an out-of-the box working module that can be customized by other developers but doesn't have to be.

## Why

One of the biggest frustrations when integrating multiple scripts together into one website is that most of the time they are not designed to easily be integrated with other scripts, even when they are advertised as being only a component of a website. Even if the integration is actually fairly easy to do, it is often hard to find where to make the appropriate changes.

For example, you may have a third-party script that will display financial data or manage a to do list. These often come with their own theme, database structure, etc. Some are easy to integrate with the rest of the website, depending on how they are structured, but it can be a nightmare if the code is complex and not well-documented.

By building your plugin or module around set concepts, it is easier to integrate into existing PHP scripts, while still giving the freedom to to code how you want.

We plan on using these concepts and example code for any plugins or modules we want to use on multiple websites.

## Concepts

There are a number of concepts behind the model:

* If the existing website is already using a login management system, you can drop in code that allows your module to use the existing login system (detect who is logged in, show or hide content based on user or user group, customize content based on user variables, etc.).
* If the existing website has its own theme, you can drop in code that either directly references the existing theme, or allows you to emulate that theme but adding the appropriate HTML.
* If the website is using its own database structure, allow the modules to use existing tables and fields, where appropriate and available.
* If the website uses libraries and other third-party code, it is easy to manage. For example, a developer can use the bootstrap code included with the module, or reference the bootstrap code that is already installed on the main website.
* Provide well documented code so that developers can easily find where to make the approriate changes.

In addition, this project strives to provide example code that can be used to speed up develeopment of commmon features.

### Database Access

* Code to access the database is located in an include file.
* Code can easily be swapped out or modified so that it references specific tables and fields.
* Any pulls from the database should use variables instead of direct references to database fields, so that it is easy to change the database structure.

### Security and Login

* Code to detect who is logged in and what permissions they have are located in an include file.
* It is easy to change how it detects who is logged in and access permissions by dropping in the appropriate code.
* The module can provide its own login system if the main website does not have one, but it should be easy to replace if the developer wishes to use an existing login system.

### Theme and CSS

* Header and footer files are located in their own include files (and subfiles).
* Developer can include existing theme files, if compatible, by referencing them in the appropriate place.
* If the theme from main website is not compatible, the developer can "emulate" the theme by creating headers and footers that look identical to the main website, but are actually a separate code base.
* Module can come with its own theme, but it can be modified or replaced by the main website's theme.

### Frameworks and Third-Party Dependancies 

* If the module uses a third-party framework, such as bootstrap, the developer can choose which version to use (the one that came wiuth the module, or the one that already exists on the existing website).

### Documentation & Comments

* Clear directions on where to make changes should be provided.
* Example code for possible changes is recommended.
* You should avoid assuming knowledge, so assume the user is just going to copy and paste some code and then modify it.
* If complex concepts and references are needed, provide links to relevant resources.

## Contribution & Usage

We are providing these concepts and example code with the hope that you find it useful. You are welcome to contribute to the code, and use it in your own projects, commercial and non-commercial.

You do not have to provide or share the source code of modules that you develop, however, we would appreciate if you contribute non-proprietory changes to the framework so that others can benefit as well.

We do ask that you keep a link to this repository in your source code, both for your own reference, and so that other developers on your project can access the original code. If you significantly modify it, you should say so near the link to this repository.

## Random Notes

#### Amusing Accidental Definition

The acronym accidentally spells out "pis&eacute;" which happens to be approrpiate.

Pis&eacute; - NOUN
1. Building material of stiff clay or earth, forced into forms that are removed as it hardens.
2. Rammed earth.

ORIGIN late 18th century: French, literally ‘pounded’

USAGE: His house was made of pis&eacute;.
