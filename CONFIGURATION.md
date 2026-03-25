# CONFIGURATION

kickers uses [direnv](https://direnv.net/) for configuration.

# PREREQUISITES

* [direnv](https://direnv.net/) 2

## Recommended

* [git](https://git-scm.com/)
* [bash](https://www.gnu.org/software/bash/) 4+

## Per-Repository Scripts

```console
% cd <project>
% mkdir -p .kickers
% cp .../kickers/sample.envrc ~/.envrc
% direnv allow
% cp .../kickers/.kickers/kick .kickers
% chmod +x .kickers/kick
```

## Per-User Scripts

```console
% mkdir -p ~/.kickers
% cp global.envrc ~/.envrc
% direnv allow
% cp kickers/.kickers/kick ~/.kickers
% chmod +x ~/.kickers/kick
```
