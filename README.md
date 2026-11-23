# kickers: SDLC workflow automators

[![CI/CD](https://badgen.net/github/checks/mcandre/kickers?icon=github)](https://github.com/mcandre/kickers/actions) [![License](https://badgen.net/static/license/BSD/ab2b29?icon=freebsd)](LICENSE.md) [![AI](https://badgen.net/static/人/NO%20AI?color=aa4a44)](AI-DECLARATION.md)

![shoe wall](kickers.png)

# SUMMARY

kickers provides a framework for per-repository, per-user scripts.

# EXAMPLE

```console
% kick
Everything up-to-date
```

# DOWNLOAD

## Per-Repository Scripts

1. Copy a `.kickers` scripts directory to your local repository.

    ```console
    % git clone https://github.com/mcandre/kickers.git ~/src/github.com/mcandre/kickers
    % cp -r ~/src/github.com/mcandre/kickers/.kickers <your-repository>
    ```

2. Register the `.kickers` directory with direnv.

    .envrc:

    ```sh
    DIR="$(dirname "$1")"
    PATH_add "${DIR}/.kickers"
    ```

3. Allowlist direnv.

    ```sh
    direnv allow
    ```

## Per-User Scripts

1. Copy a `.kickers` scripts directory to your home directory.

    ```console
    % git clone https://github.com/mcandre/kickers.git ~/src/github.com/mcandre/kickers
    % cp -r ~/src/github.com/mcandre/kickers/.kickers ~
    ```

2. Register the `.kickers` directory with direnv.

    .envrc:

    ```sh
    PATH_add "${HOME}/.kickers"
    ```

3. Allowlist direnv.

    ```sh
    direnv allow
    ```

# PREREQUISITES

* [direnv](https://direnv.net/) 2
* [git](https://git-scm.com/)

## Recommended

* [bash](https://www.gnu.org/software/bash/) 4+

For details on building from source, see [DEVELOPMENT](DEVELOPMENT.md).

👟
