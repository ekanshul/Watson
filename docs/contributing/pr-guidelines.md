# Pull request guidelines

> *nota bene*
>
> Open a pull request even if your contribution is not ready yet! It can
> be discussed and improved collaboratively! You may prefix the title of
> your pull request with "WIP: " to make it clear that it is not yet ready
> for merging.

Before we merge a pull request, we check that it meets these guidelines:

1. Please, write
    [commit messages that make sense](https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html),
    and
    [rebase your branch](https://git-scm.com/book/en/v2/Git-Branching-Rebasing)
    before submitting your pull request.
2. We may ask you to
    [squash your commits](http://gitready.com/advanced/2009/02/10/squashing-commits-with-rebase.html)
    too. This is used to "clean" your pull request before merging it (we don't
    want commits such as `fix tests`, `fix 2`, `fix 3`, etc.). Pull requests
    containing `fixup!` commits are rejected by the CI.
3. While creating your pull request on GitHub, you **must** write a
   description which gives the context and/or explains why you are
   creating it.
4. The pull request **should** include tests.
5. If the pull request adds functionality, the docs **should** be
   updated.
6. The pull request **must** update the `## [Unreleased]` section of
   `CHANGELOG.md`.
7. *GitHub Actions* checks should be **green** :) They make sure the linters
   and the tests pass with every supported version of Python.

Thank you!
