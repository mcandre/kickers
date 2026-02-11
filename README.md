# kickers: SDLC workflow automators

[![license](https://img.shields.io/badge/license-BSD-3)](LICENSE.md) [![Donate](https://img.shields.io/badge/-any?logo=gumroad&label=Donate&color=grey)](https://mcandre.gumroad.com/)

# ABOUT

kickers automate common development workflows.

Workflows are customizable on a per-user and/or per-repository basis.

# EXAMPLE

```console
$ kick
Everything up-to-date
```

The example [.kickers/kick](.kickers/kick) script automates common git operations, such as syncing the current git branch between local and remote repositories.

See `kick -h` for more options.

# REQUIREMENTS

* [direnv](https://direnv.net/) 2

## Recommended

* [git](https://git-scm.com/) 2.46.1+
* [GNU bash](https://www.gnu.org/software/bash/) 4+

# SETUP

1. Install direnv.
2. Register some per-user and/or per-project kicker scripts.

## PER-USER KICKER SCRIPTS

Per-user kicker scripts apply to most of your local projects.

```console
$ mkdir -p ~/.kickers
$ cp global.envrc ~/.envrc
$ direnv allow
$ cp kickers/.kickers/kick ~/.kickers
$ chmod +x ~/.kickers/kick
```

## PER-PROJECT KICKER SCRIPTS

Per-project scripts apply to specific project(s), and may override per-user scripts based on the script basename.

```console
$ cd <project>
$ mkdir -p .kickers
$ cp .../kickers/sample.envrc ~/.envrc
$ direnv allow
$ cp .../kickers/.kickers/kick .kickers
$ chmod +x .kickers/kick
```

👟
