---
title: mender-connect
taxonomy:
    category: docs
shortcode-core:
    active: false
github: false
---

## mender-connect 1.2.0

_Released 07.14.2021_

### Statistics

A total of 2823 lines added, 957 removed (delta 1866)

| Developers with the most changesets | |
|---|---|
| Alf-Rune Siqveland | 8 (40.0%) |
| Ole Petter Orhagen | 5 (25.0%) |
| Peter Grzybowski | 4 (20.0%) |
| Manuel Zedel | 2 (10.0%) |
| Kristian Amlie | 1 (5.0%) |

| Developers with the most changed lines | |
|---|---|
| Peter Grzybowski | 1949 (64.8%) |
| Alf-Rune Siqveland | 862 (28.7%) |
| Ole Petter Orhagen | 152 (5.1%) |
| Manuel Zedel | 42 (1.4%) |
| Kristian Amlie | 1 (0.0%) |

| Top changeset contributors by employer | |
|---|---|
| Northern.tech | 20 (100.0%) |

| Top lines changed by employer | |
|---|---|
| Northern.tech | 3006 (100.0%) |

| Employers with the most hackers (total 5) | |
|---|---|
| Northern.tech | 5 (100.0%) |

### Changelogs

#### mender-connect (1.2.0)

New changes in mender-connect since 1.1.0:

* stat(2) file path and verify conditions before starting upload
* Add option to pass src_path to file upload requests
* FIX: Filetransfer owner restrictions checks username not (optional) real-name
* A Fix for group and owner file transfer limits
* Fix the terminal PATH issues in the standard shell by defaulting to
  starting a 'login' shell with the '--login' option. This can be controlled
  through the new configuration field 'ShellArguments', which you can set to
  whatever arguments you want passed to the shell on startup.
  ([MEN-4505](https://tracker.mender.io/browse/MEN-4505))
* Handle the re-connection request even if there is
  no new JWT token from the Mender client
  ([MEN-4694](https://tracker.mender.io/browse/MEN-4694))

## mender-connect 1.1.0

_Released 04.16.2021_

### Changelogs

#### mender-connect (1.1.0)

New changes in mender-connect since 1.0.0:

* Add remote triggers for Mender client's check-update and send-inventory
* [examples/mender-connect.conf] Remove unnecessary ServerURL
* Add handler for File Transfer protocol.
([MEN-4322](https://tracker.mender.io/browse/MEN-4322))
* filetransfer: Add handler for fetching file and file info
* New feature: TCP and UDP port-forwarding
* stat(2) file path and verify conditions before starting upload
* Add option to pass src_path to file upload requests

## mender-connect 1.0.1

_Released 16.04.2021_

### Changelogs

#### mender-connect (1.0.1)

New changes in mender-connect since 1.0.0:

* [examples/mender-connect.conf] Remove unnecessary ServerURL


## mender-connect 1.0.0

_Released 01.20.2021_

### Changelogs

#### mender-connect (1.0.0)

* First release of mender-connect

