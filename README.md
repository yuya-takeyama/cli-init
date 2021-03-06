cli-init [![Build Status](https://drone.io/github.com/tcnksm/cli-init/status.png)](https://drone.io/github.com/tcnksm/cli-init/latest) [![Coverage Status](https://coveralls.io/repos/tcnksm/cli-init/badge.png)](https://coveralls.io/r/tcnksm/cli-init) [![MIT License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat)](https://github.com/tcnksm/cli-init/blob/master/LICENCE)
====

The easy way to start building Golang command-line application.

## Description

`cli-init` is the easy way to start building Golang command-line application with [codegangsta/cli](https://github.com/codegangsta/cli). All you need to do is to set application name and its subcommand. `cli-init` generates its templates (scaffold) which you need to write when using codegangsta/cli. You can focus on core functionality of application.

## Demo

![](http://deeeet.com/writing/images/post/cli-init.gif)

## Usage

You just need to set its application name:

```bash
$ cli-init [options] [application]
```

You can set subcommands with `-s` option:

```bash
$ cli-init -s subcommand1,subcommand2,subcommand3 [application]
```

## Artifacts

`cli-init` generates templates (scaffold) which you need to write when using [codegangsta/cli](https://github.com/codegangsta/cli):

- **main.go** - defines main function. It includes application name, version, usage, author name and so on. 
- **commands.go** - defines sub-commands. It includes subcommand name, usage, function and so on. 
- **version.go** - defines application version. default value is `0.1.0`
- **README.md** - insctructs application name, synopsis, usage and installation and so on. 
- **CHANGELOG.md** - shows version release date and its updates.

See more details [codegangsta/cli](https://github.com/codegangsta/cli).

## Example

If you want to start to building `todo` application which has subcommands `add`, `list`, `delete`:

```bash
$ cli-init -s add,list,delete todo
```

You can see sample of artifacts in [tcnksm-sample/cli-init](https://github.com/tcnksm-sample/cli-init).

## Installation

To install, use `go get` and `make install`. We tag versions so feel free to checkout that tag and compile.

```bash
$ go get -d github.com/tcnksm/cli-init
$ cd $GOPATH/src/github.com/tcnksm/cli-init
$ make install 
```

## Contribution

1. Fork ([https://github.com/tcnksm/cli-init/fork](https://github.com/tcnksm/cli-init/fork))
1. Create a feature branch
1. Commit your changes
1. Rebase your local changes against the master branch
1. Run test suite with the `go test ./...` command and confirm that it passes
1. Run `gofmt -s`
1. Create new Pull Request

## Author

[tcnksm](https://github.com/tcnksm)
