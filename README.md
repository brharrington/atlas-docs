[![Build Status](https://travis-ci.org/Netflix/atlas-docs.svg)](https://travis-ci.org/Netflix/atlas-docs/builds)

# Atlas Docs

Experiment for moving [Atlas] documentation off of GitHub wiki and unifying with the
[Spectator] documentation. Goals:

* Avoid duplication and confusion about what information should go in Atlas wiki or
  Spectator docs.
* Provide unified search across both docs.
* Support for extensions to render Atlas graphs and format expressions. Currently this
  is done by `atlas-wiki` subproject.
* Fix some of the limitations of GitHub wiki such as page naming and ability to simply
  link to operators by substituting in the name.
* Make it easier for others to contribute to the docs.

[Atlas]: https://github.com/Netflix/atlas/
[Spectator]: https://github.com/Netflix/spectator/

# Operations

## Development

Setup a virtual environment with the appropriate Python libraries:

```
./setup-venv.sh
source venv/bin/activate
```

The following command will build and serve the docs locally on port 8000:

```
mkdocs serve
```

See the [Atlas Formatting Plugin README] for details on using directives in Markdown source.

See the [Atlas Link Checker README] for details on validating links in MkDocs site output.

[Atlas Formatting Plugin README]: ./plugins/mkdocs-atlas-formatting-plugin/README.md
[Atlas Link Checker README]: ./plugins/atlas-link-checker/README.md

## Travis Build and Deploy

The following blog post details the process used here, based on GitHub Deploy Keys, so that write
access is restricted to this repository:

* [Deploying Docs on Github with Travis-CI](https://derekweitzel.com/2017/02/08/deploying-docs-on-github-with-travisci/)
