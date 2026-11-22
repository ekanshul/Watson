![Watson Logo](https://jmaupetit.github.io/Watson/img/logo-watson.svg)

![PyPI - Version](https://img.shields.io/pypi/v/td-watson)

Watson is here to help you manage your time. You want to know how much time you
are spending on your projects? You want to generate a nice report for your
client? Watson is here for you.

Wanna know what it looks like? Check this below.

[![Watson demo](https://jmaupetit.github.io/Watson/img/watson-demo.gif)](https://asciinema.org/a/35918)

Nice, isn't it?

## Quick start

### Installation

The easiest way to install Watson is to use [uv](https://docs.astral.sh/uv/):

```sh
$ uv tool install td-watson
```

This will create a Python virtual environment for Watson and a shortcut
available in your `$PATH`.

Alternatively, you may use pip inside a virtual environment:

```sh
$ pip install td-watson
```

On macOS, a [Homebrew](https://brew.sh/) formula is also available:

```sh
$ brew update && brew install watson
```

If you need more details about installing Watson, please refer to the
[documentation](https://jmaupetit.github.io/Watson).

### Usage

Start tracking your activity via:

```sh
$ watson start world-domination +cats
```

With this command, you have started a new **frame** for the *world-domination*
project with the *cats* tag. That's it.

Now stop tracking your world domination plan via:

```sh
$ watson stop
Stopping project world-domination [cats], started 8 minutes ago and stopped just now. (id: ffb2a4c)
```

You can log your latest working sessions (aka *frames*) thanks to the `log`
command:

```sh
$ watson log
Tuesday 26 January 2016 (8m 32s)
      ffb2a4c  13:00 to 13:08      08m 32s   world-domination  [cats]
```

Please note that, like the
[`report` command](https://jmaupetit.github.io/Watson/user-guide/commands/#report),
the `log` command can filter by project, tag and date.

To list all available commands, either [read the
documentation](https://jmaupetit.github.io/Watson) or use:

```sh
$ watson help
```

## Contributor Code of Conduct

If you want to contribute to this project, please read the project [Contributor
Code of Conduct](https://jmaupetit.github.io/Watson/contributing/coc/).

## License

Watson is released under the MIT License. See the bundled LICENSE file for
details.
