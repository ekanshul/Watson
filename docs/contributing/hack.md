# Hack

Ready to contribute? Here's how to set up _Watson_ for local development.

## Python requirements

- Python 3.11+
- [uv](https://docs.astral.sh/uv/) package manager

## Get started!

1. Fork the [Watson repository](https://github.com/jmaupetit/Watson/) on GitHub.

2. Clone your fork locally:

        $ git clone git@github.com:your_name_here/Watson.git

3. Create a virtual environment and install project dependencies:

        $ cd Watson
        $ make bootstrap

4. Create a branch for local development:

        $ git checkout -b name-of-your-bugfix-or-feature

    Now you can make your changes locally.

    _Notes:_

    - The files you need to edit to change Watson's behavior are located in the
      `watson/` subfolder.
    - Every time you use `uv run watson`, the source code inside the `watson/`
      subfolder will be used.
    - To avoid messing with your real Watson data, set the `WATSON_DIR`
      environment variable to another
      [application folder](../user-guide/configuration.md#application-folder),
      e.g. `export WATSON_DIR=/tmp/watson`. You can run `uv run watson projects`
      to check that your real projects are not shown.

5. When you're done making changes, check that they pass the linters and the
   tests (see [Run the tests](#run-the-tests)):

        $ make lint
        $ make test

6. If you have added a new command or updated/fixed docstrings, please
   regenerate the commands documentation. You can check changes live using
   `make docs-serve`:

        $ make docs-serve

7. Describe your changes in the `## [Unreleased]` section of `CHANGELOG.md`
   (this is checked by the CI).

8. Commit your changes and push your branch to GitHub:

        $ git add .
        $ git commit -m "Your detailed description of your changes."
        $ git push -u origin name-of-your-bugfix-or-feature

9. After [reading this](./pr-guidelines.md), submit a pull request through the
   GitHub website.

## Run the tests

The tests use [pytest](https://docs.pytest.org/). To run them with the default
Python interpreter, use:

    $ make test

If you want to run pytest with custom options, use:

    $ uv run pytest -x -k test_cli
