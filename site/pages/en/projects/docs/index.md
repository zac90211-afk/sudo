---
page_ref: "@ARK_PROJECT__VARIANT@/agnostic-apollo/sudo/docs/@ARK_DOC__VERSION@/index.html"
ark__replacement_strings:
  - target: "../releases/index.md"
    replacement: "@ARK_PAGE__URL@/../../../releases/index.html"
---

# sudo Docs

<!-- @ARK_DOCS__HEADER_PLACEHOLDER@ -->

[`sudo`](https://github.com/agnostic-apollo/sudo) stands for *superuser do*. It is a wrapper script to execute commands as the `root (superuser)` user in the [Termux](https://github.com/termux/termux-app) app, like to drop to an interactive shell for any of the [supported shells](usage/index.md#supported-shells), or to execute shell script files or their text passed as an argument.

### Contents

- [Releases](../releases/index.md)
- [Install](install/index.md)
- [Usage](usage/index.md)
- [Developer](developer/index.md)
  - [Build](developer/build/index.md)
  - [Test](developer/test/index.md)
  - [Contribute](developer/contribute/index.md)
- [Introduction](#introduction)
- [Changelog](#changelog)
- [License](https://github.com/agnostic-apollo/sudo/blob/master/LICENSE)

---

&nbsp;




## Introduction

First of all, please read the [Termux](https://github.com/termux/termux-app) app docs, so that you will have a basic understanding of how the app works.

The most important functions provided by `sudo` are "interactive shell" and "command execution".

### Interactive Shell

Drop to an interactive shell of any of the [supported shells](usage/index.md#supported-shells) as the `root` user, with the Termux environment set up in the root shell.

### Command Execution

Execute commands, shell script files, or their text passed as an argument as the `root` user.

---

&nbsp;




## Changelog

### v1.2.0

- Fixed passing the `--interactive` flag along with `-c` to force open a tty as required by Magisk now.
- Fixed calling `sudo_set_su_variables()` before running tests to properly set `ANDROID_PATH`.

### v1.1.0

- Added `riscv64` support.
- Changed version string output to standardized format.

### v1.0.0

- Added support for Termux `TERMUX_` scoped environment variables for dynamic path resolution.
- Added support for Android 5/6.
- Added `-A`, `-AA`, `-t`, `-T`, `-TT` priority flags for controlling `PATH` and `LD_LIBRARY_PATH`.

---

&nbsp;
