# Kinja Development Guidelines

This document provides the guidelines to be followed by third-party developers engaged by Kinja Digital for projects.

1. Project management flow
2. Development flow
3. PHP standards
4. JS standards

---

## Project management flow

### Backlog management

We use [Trello](https://www.trello.com) to manage our projects.

Each Trello board is set up with the following lanes:

* **Backlog**: all the work that needs to be done, but hasn’t yet been completed. Cards usually include references to the requirements in Google Docs, as well as diagrams and/or wireframes of the desired outcome for each card.
* **Blocked**: tasks that were started by someone, but cannot be completed because more information is required or another task needs to be completed first. A major priority for the project manager is to make sure "blocked" items are unblocked and moved to "backlog" (and subsequently "In progress") as quickly as possible.
* **In Progress**: tasks that a team member is currently working on. An important rule: each team member should have one and only one item in this lane at any time.
* **QA**: when a team member has finished a task, they move it to "QA." The project manager will then test the functionality to make sure it’s working and then move the task into:...
* **Done**: completed tasks. Cards in this lane get archived on a weekly basis.

The workflow is illustrated below:

![Trello workflow](http://coreymcmahon.com/wp-content/uploads/2015/01/developer-workflow.png)




### Team communication

All team communication is handled using [Slack](https://www.slack.com). 

* A channel for each project
* A channel for general discussion
* A channel for (automated) project related alerts

Daily "stand up"

1. What did I accomplish yesterday?
2. What will I focus on today?
3. What obstacles are impeding my progress?

End of day status update

---

## Development flow

### Branching strategy

The repository origin will have two primary branches:

* `master` has the code for the latest release
* `develop` has the code that is being worked on but not yet released

All development should be done in **feature branches**, which are pushed up to the shared `origin` remote at the end of each day. Each feature branch should be named to reference a Trello card number. For example: `feature/12-add-drop-down`.

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