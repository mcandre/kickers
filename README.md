# kickers: SDLC workflow automators

[![license](https://img.shields.io/badge/license-BSD-3)](LICENSE.md)

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
