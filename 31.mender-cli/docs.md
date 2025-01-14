---
title: mender-cli
taxonomy:
    category: docs
shortcode-core:
    active: false
github: false
---

## mender-cli 1.7.0

_Released 04.16.2021_

### Changelogs

#### mender-cli (1.7.0)

New changes in mender-cli since 1.6.0:

* Fix: Respect the --server flag from config everywhere
* `mender-cli --record <my-file> terminal <DEVICE-ID>` records
the terminal session into a local file.
([MEN-4318](https://tracker.mender.io/browse/MEN-4318))
* `mender-cli --playback <my-file> terminal` playbacks the
previously recorded terminal session from a local file.
([MEN-4318](https://tracker.mender.io/browse/MEN-4318))
* New command `mender-cli devices list` to list all devices
from /devauth/devices endpoint. The amount of detail can be controlled
using cli parameter `-d/--detail`, same as for other commands.
* Previously, the --generate-autocomplete call would silently ignore
errors, when the autocomplete directory was not present. This explicitly logs
the errors returned during autocomplete script generation.
* New command port-forward: port-forward TCP and UDP ports from the device
* Add filetransfer upload and download support
([MEN-4323](https://tracker.mender.io/browse/MEN-4323))
* Aggregated Dependabot Changelogs:
* Bumps golang from 1.15.6-alpine3.12 to 1.15.8-alpine3.12.
* Bumps [github.com/spf13/cobra](https://github.com/spf13/cobra) from 1.1.1 to 1.1.3.
- [Release notes](https://github.com/spf13/cobra/releases)
- [Changelog](https://github.com/spf13/cobra/blob/master/CHANGELOG.md)
- [Commits](https://github.com/spf13/cobra/compare/v1.1.1...v1.1.3)
* Bumps [github.com/cheggaaa/pb/v3](https://github.com/cheggaaa/pb) from 3.0.5 to 3.0.6.
- [Release notes](https://github.com/cheggaaa/pb/releases)
- [Commits](https://github.com/cheggaaa/pb/compare/v3.0.5...v3.0.6)
* Bumps golang from 1.15.8-alpine3.12 to 1.16.0-alpine3.12.
* Bumps golang from 1.16.0-alpine3.12 to 1.16.2-alpine3.12.
* Bumps [github.com/cheggaaa/pb/v3](https://github.com/cheggaaa/pb) from 3.0.6 to 3.0.7.
- [Release notes](https://github.com/cheggaaa/pb/releases)
- [Commits](https://github.com/cheggaaa/pb/compare/v3.0.6...v3.0.7)

## mender-cli 1.6.1

_Released 16.04.2021_

### Changelogs

#### mender-cli (1.6.1)

New changes in mender-cli since 1.6.0:

* Fix: Respect the --server flag from config everywhere

## mender-cli 1.6.0

_Released 01.20.2021_

### Changelogs

#### mender-cli (1.6.0)

New changes in mender-cli since 1.5.0:

* Fix login with password, and improve the configuration file handling
* Add 'artifact list' command to list Artifacts on the Mender server
* Prompt for the users username if not provided on the CLI
* Add '--version' option to display the current mender-cli version
* New CLI command "terminal" to access a device's remote terminal
* mender-cli requires now golang 1.15 or newer
* Aggregated Dependabot Changelogs:
* Bumps golang from 1.14-alpine3.12 to 1.15.1-alpine3.12.
* Bump golang from 1.14-alpine3.12 to 1.15.1-alpine3.12
* Bumps golang from 1.15.1-alpine3.12 to 1.15.2-alpine3.12.
* Bump golang from 1.15.1-alpine3.12 to 1.15.2-alpine3.12
* Bumps [github.com/cheggaaa/pb/v3](https://github.com/cheggaaa/pb) from 3.0.4 to 3.0.5.
- [Release notes](https://github.com/cheggaaa/pb/releases)
- [Commits](https://github.com/cheggaaa/pb/compare/v3.0.4...v3.0.5)
* Bump github.com/cheggaaa/pb/v3 from 3.0.4 to 3.0.5
* Bumps golang from 1.15.2-alpine3.12 to 1.15.3-alpine3.12.
* Bumps [github.com/spf13/cobra](https://github.com/spf13/cobra) from 1.0.0 to 1.1.1.
- [Release notes](https://github.com/spf13/cobra/releases)
- [Changelog](https://github.com/spf13/cobra/blob/master/CHANGELOG.md)
- [Commits](https://github.com/spf13/cobra/compare/v1.0.0...v1.1.1)
* Bump golang from 1.15.2-alpine3.12 to 1.15.3-alpine3.12
* Bump github.com/spf13/cobra from 1.0.0 to 1.1.1
* Bumps golang from 1.15.3-alpine3.12 to 1.15.4-alpine3.12.
* Bump golang from 1.15.3-alpine3.12 to 1.15.4-alpine3.12
* Bumps golang from 1.15.4-alpine3.12 to 1.15.5-alpine3.12.
* Bump golang from 1.15.4-alpine3.12 to 1.15.5-alpine3.12
* Bumps golang from 1.15.5-alpine3.12 to 1.15.6-alpine3.12.
* Bump golang from 1.15.5-alpine3.12 to 1.15.6-alpine3.12

## mender-cli 1.5.1

_Released 01.21.2021_

### Changelogs

#### mender-cli (1.5.1)

New changes in mender-cli since 1.5.0:

* Fixed login with password


## mender-cli 1.5.0

_Released 09.11.2020_

### Changelogs

#### mender-cli (1.5.0)

New changes in mender-cli since 1.4.0:

* Add: Make the server flag default to hosted Mender
* Add: Bash auto-completion functionality
* Add: Zsh auto-completion support
* Add: Configuration file functionality
This adds the possibility to add the username and password to a configuration
file, in which the 'mender-cli' tool will look if no password or username is set
on the CLI. The configuration file is expected to be JSON.
The configuration file can be located in one of:
* /etc/mender-cli
* $HOME
* . (directory where binary is run from)
and must be named like:
```console
.mender-clirc.json
```
This helps usage, in that now, in order to login, a user with a configuration
file can do:
```console
$ mender-cli login
```
as opposed to:
```console
$ mender-cli --username foo --password bar --server bar.com
```
The parameters which are configurable from the config file are:
* username
* password
* server

## mender-cli 1.4.1

_Released 16.04.2021_

### Changelogs

#### mender-cli (1.4.1)

New changes in mender-cli since 1.4.0:

* Bump golang version to 1.14-alpine3.12


## mender-cli 1.4.0

_Released 07.15.2020_

### Changelogs

#### mender-cli (1.4.0)

New changes in mender-cli since 1.3.0:

* Support for two factor authentication token for login
([MEN-3176](https://tracker.mender.io/browse/MEN-3176))
* Change the name of the two-factor auth option.

## mender-cli 1.3.0

_Released 03.05.2020_

### Changelogs

#### mender-cli (1.3.0)

New changes in mender-cli since 1.2.0:

* Build and publish Mac OS X binary for `mender-cli`

## mender-cli 1.2.0

_Released 09.16.2019_

### Changelogs

#### mender-cli (1.2.0)

New changes in mender-cli since 1.1.0:

* Store login token in XDG Basedir Spec Cache-directory
([MEN-2387](https://tracker.mender.io/browse/MEN-2387))

