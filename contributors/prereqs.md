---
layout: documentation
title:  Prerequisites
order: 1
---

Phovea is built on a range of standard technologies: Contributors to Phovea should be familiar
with the tools we're already using.

- Understanding what's already in place may save you from reinventing the wheel,
or adding an extra wheel.
- Understanding the idioms of the tool you're working with will make your code more clear
to future developers.

## Technologies and Tools used in Phovea

### Programming Languages

**Client**

* [TypeScript 2](http://www.typescriptlang.org/)
* [SASS](http://sass-lang.com/)

**Server**

* [Python](https://python.org)

### Frameworks / Libraries

**[Phovea Generator](https://github.com/phovea/generator-phovea)**

* yeoman

**Client**

* [D3](https://d3js.org)
* [Font Awesome](http://fontawesome.io/)
* [Bootstrap 3](http://getbootstrap.com/)
* [Jasmine](https://jasmine.github.io/) for testing
* Now and then: [LineUp.js](https://github.com/Caleydo/lineupjs), [Papa Parse](http://papaparse.com/), [jQuery](https://jquery.org) [select2](https://github.com/select2/select2), [moment](http://momentjs.com/), [lodash](https://lodash.com/docs), ...

**Server**

* [flask](http://flask.pocoo.org/)
* [pytest](http://docs.pytest.org/en/latest/) for testing
* Now and then: [numpy](http://www.numpy.org/), [pandas](http://pandas.pydata.org/), [Requests](http://docs.python-requests.org/en/master/), [Celery](http://www.celeryproject.org/), [LDAP](https://www.python-ldap.org/), ...


### Data Stores

* [Redis](https://redis.io/)
* [MongoDB](https://www.mongodb.com/)
* [Hierarchical Data Format](https://www.hdfgroup.org/) (HDF)
* [SQLAlchemy](http://www.sqlalchemy.org/) -> [PostgreSQL](https://www.postgresql.org/), [SQlite](https://sqlite.org/), [MySQL](https://www.mysql.com/)
* [Neo4j](https://neo4j.com)

### Build Tools

* [Webpack 2](https://webpack.js.org/)
* [Karma Test Runner](https://karma-runner.github.io/)
* [pytest runner](https://pypi.python.org/pypi/pytest-runner)
* [Python setuptools](https://pypi.python.org/pypi/setuptools)
* [Travis CI](https://travis-ci.org/)


## Version Control

All source code and documentation for Phovea is hosted on [Github](https://github.com/phovea).
Projects built with Phovea as part of the Caleydo project can be found in the distinct [Caleydo](https://github.com/caleydo)
organization on Github. 

If you haven't used git itself before, please read through
[this tutorial](https://git-scm.com/docs/gittutorial),
or try this [interactive one](https://try.github.io/).

To make contributions, please make sure you're up to date, and then branch from *master*.
When you're done, make a pull request (PR) for your branch on Github. The primary maintainer for
each project should keep an eye on issues and PRs as they come in, but feel free to nudge them:

| repo                         | primary   | backup       |
|------------------------------|-----------|--------------|
| phovea.github.io             | @mccalluc | @aaljuhani   |
|
| generator-phovea             | @sgratzl  | @cnobre      |
| phovea_bootstrap_fontawesome | @thinkh   | @mccalluc    |
| phovea_core                  | @thinkh   | @sgratzl
| phovea_importer              | @thinkh   | @aaljuhani |
| phovea_bundle_lib            | @sgratzl  | @mccalluc    |
| phovea_clue                  | @thinkh   | @cnobre      |
| phovea_processing_queue      | @thinkh   | @bikramkawan |
| phovea_security_flask        | @sgratzl   | @aaljuhani   |
| phovea_server                | @sgratzl  | @bikramkawan |
| phovea_data_*                | @thinkh   | @pkerpedjiev |
| phovea_graph_dot             | ?   | @cnobre      |
| phovea_vis / phovea_d3       | @thinkh   | @mccalluc    |
| phovea_vis_lineup            | ?   | @pkerpedjiev |
|
| Caleydo/lineup.js            | @sgratzl   | ? |
| sgratzl/lineup_demos         | ?   | @pkerpedjiev |
| Caleydo/taco*                | @thinkh   | @aaljuhani   |
| Caleydo/targid_ppi           | @mstreit   | @cnobre      |
| Caleydo/targid*              | @mstreit   | @bikramkawan |
| Caleydo/stratomex_js         | @thinkh   | @aaljuhani   |
| Caleydo/domino_js            | @thinkh   | @bikramkawan |
|
| Caleydo/pathfinder           | ?   |
| Caleydo/vials                | ?   |

Maintainers for each project have responsibilities:

- As issues come in, make sure labels are assigned.
- Try to reproduce bugs and make sure the recipes provide enough information.
- Assign issues to the best person to do the work.
- Review code during pull requests.
- Fix the master branch if it breaks.
- Run `yo phovea:update` as requested by `phovea-generator` folks.
- Keep the documentation up to date.

As the project develops we will used tagged releases, following
[semantic versioning](http://semver.org/) conventions, but that is not necessary for every merge.

## Documentation

Each Phoveo repo has a brief README, but documentation of the over-all project can be found here,
as you've already discovered. The source code for the documentation is itself available
[on github](https://github.com/phovea/phovea.github.io). 

READMEs, this documentation, and Github
issue reports all use [Markdown](https://guides.github.com/features/mastering-markdown/).
Although HTML can be used within Markdown, it is usually not a good idea.

This documentation is hosted by the [Github pages](https://pages.github.com/) platform: Beyond the
basic Markdown, [Jekyll](https://jekyllrb.com/) and
[Liquid Templates](http://shopify.github.io/liquid/basics/introduction/) are used to create a
complete site. If you are just contributing documentation, these details won't matter, except for
one gotcha: New pages must include YAML front matter if they are to be recognized by Jekyll.
At the top of each file there should be lines like this:

```
---
layout: documentation
title:  Prerequisites
order: 1
---
```

If you find a mistake in the documentation, please correct it. For small edits, it might be easier
to use Github's online editor, but please do save your changes in a branch and create a PR, rather
than committing to master: This gives the system time to do a basic syntax check.

## Packaging

We are using NPM's [`package.json`](https://docs.npmjs.com/files/package.json) to manage dependencies between components and external (web) libraries. Phovea plugins can be published to the NPM registry. Note, however, that we are *not* using the Node.js
language.

New projects can be created with the [Phovea Generator](https://github.com/phovea/generator-phovea/) that is a [Yeoman](http://yeoman.io/) generators.
See our [cheatsheet](/contributors/cheatsheet/) for more details.

## Server

Server-side plugins use the Python [Flask](http://flask.pocoo.org/) framework. However, if these plugins register namespaces any WSGI compliant Python framework could be used.

## Client

Client-side code is written in [TypeScript](https://www.typescriptlang.org/) and then compiled down
to Javascript. TypeScript adds a typesystem to Javascript, and also lets you use features of the newest
versions of the ECMAScript even on older browsers.  As part of the build process, multiple libraries and assets
are combined using [Webpack](https://webpack.github.io/).

The visualizations in Phovea are created (mostly) with [D3](https://github.com/d3/d3/wiki).

[JavaScript Promises](https://developers.google.com/web/fundamentals/getting-started/primers/promises)
are used throughout Phovea. The main idea of Promises is that asynchronous processes can be handled in
code that can still be read lineary. At some points in Phovea a Promise is returned even is a value is
immediately available, because we wanted to accomodate instances where a query to the server
might actually be necessary.

## Testing

When you push changes to Github, tests can automatically be run with
[Travis](https://docs.travis-ci.com/user/getting-started/). If you have a new project,
two things are necessary:

- Enable the tests by flipping the switch for your repo on https://travis-ci.org/profile/phovea,
or the appropriate list for your organization. (Click the "resync" button if it is not on the
list at first.)
- Add a `travis.yml` to indicate what tests should be run.

Any program or script that can return either a zero (success) or non-zero (failure) status can be part of your
tests, but typically unit tests will be written with [Jasmine](https://jasmine.github.io/) and run
with the [Karma test runner](https://karma-runner.github.io/).
