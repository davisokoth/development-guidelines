# Kinja Development Guidelines

This document provides the guidelines to be followed by third-party developers engaged by Kinja Digital for projects.

1. (overarching principles)
2. (high level system architecture)
3. Project management flow
3. Development flow
3. PHP standards
4. JS standards

---

## Overarching principles

...

All architectural decisions [12 Factor App](http://12factor.net/)

---

## High level system architecture

...

---

## Project management flow

...

Trello

Slack

Daily "stand up"

End of day status update

---

## Development flow

### Branching strategy

The repository origin will have two primary branches:

* `master` has the code for the latest release
* `develop` has the code that is being worked on but not yet released

All development should be done in **feature branches**, which are pushed up to the shared `origin` remote at the end of each day.

When a feature (or bugfix, or story) is complete, the developer should open a pull request against the `develop` branch.

### Code reviews

At least one other member of the team must perform a code review of the pull request before it is merged. 

Approval of a pull request is acknowledged by the reviewing developer leaving a comment on the pull request with either the text `+1`, or the thumbs-up emoticon.

### Deployments

* `master` is automatically deployed to production on commit.
* `develop` is automatically deployed to the staging server on commit.

---

## PHP Standards

### Version

All of our PHP applications have PHP 5.6+ as a hard requirement.

Laravel is our framework of choice. At the time of writing the latest version is 5.2, which is what we will use for all projects moving forwards.

### Coding style

We strictly adhere to [PSR-1](http://www.php-fig.org/psr/psr-1/) and [PSR-2](http://www.php-fig.org/psr/psr-2/).

All committed code **must** be run through the [PHP coding standards fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer) tool prior to opening a pull request.

---

## JS Standards

### Dialect

We use vanilla JavaScript.

### Coding style

We use the [JavaScript Standard Style](https://github.com/feross/standard) formatting guidelines. 

**Note**: there are some (arguably) controversial opinions that JS Standard subscribes to. Among those the most notable are:

* 2 spaces for indentation
* Single quotes for strings
* **No semicolons**...

### Dependency management

Use NPM for everything. Avoid proprietary build and dependency management systems (e.g. Bower).

### Packaging

For exports, we use the **CommonJS/node.js** standard.