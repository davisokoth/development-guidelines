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

## High level system architecture

...

## Project management flow

...

Trello

Slack

Daily "stand up"

End of day status update


## Development flow

* `master` has the code for the latest release
* `develop` has the code that is being worked on but not yet released

All development should be done in **feature branches** which are pushed up to the shared remote at the end of each day.

When a feature / bugfix / story is complete, the developer should open a pull request against the `develop` branch.

At least one other member of the team must perform a code review of the pull request before it is approved and merged. Approval of a pull request is acknowledged by the reviewing developer leaving a comment on the pull request with either the text "+1", or the thumbs up emoticon.


## PHP Standards

We strictly adhere to [PSR-1](http://www.php-fig.org/psr/psr-1/) and [PSR-2](http://www.php-fig.org/psr/psr-2/).

All committed code **must** be run through the [PHP coding standards fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer) tool prior to opening a pull request.

## JS Standards

...

CommonJS/node.js

Use the [JavaScript Standard Style](https://github.com/feross/standard). 

**Note**: there are some (arguably) controversial opinions 

* 2 spaces – for indentation
* Single quotes for strings – except to avoid escaping
* No unused variables – this one catches tons of bugs!
* No semicolons – It's fine. Really!
* Never start a line with ( or [
* Space after keywords if (condition) { ... }
* Space after function name function name (arg) { ... }
* Always use === instead of == 
* Always handle the node.js err function parameter
* Always prefix browser globals with window