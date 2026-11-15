# CodeLoom

<img src=".github/images/repository-icon.png" alt="CodeLoom" width="120" align="left">

<b>CodeLoom</b> is a fast and free multi-language code editor and IDE for Android,
with a full Linux terminal, a Python runtime with package management, and Git integration.

This repository contains the complete source code and the build instructions for the project.  
You can contribute by reporting issues, suggesting features, or submitting pull requests.

![Android CI](https://github.com/wsnd/CodeLoom/workflows/Android%20CI/badge.svg) [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

## Build instructions

### Prerequisites

* At least **1,11GB** of free disk space: **144,7MB** for source codes and around **965,3MB** for
  files generated after building all variants
* **4GB** of RAM
* **macOS** or **Linux**-based operating system. **Windows** platform is supported by
  using [Git Bash](https://gitforwindows.org/).

### Building

1. `$ git clone --recursive --depth=1 --shallow-submodules https://github.com/wsnd/CodeLoom CodeLoom`
   — clone **CodeLoom** with submodules
2. In case you forgot the `--recursive` flag, `cd` into `CodeLoom` directory
   and: `$ git submodule init && git submodule update --init --recursive --depth=1`
3. Create `local.properties` file with the following properties:  
   `KEYSTORE_PATH`: absolute path to the keystore file  
   `KEYSTORE_PASSWORD`: password for the keystore  
   `KEY_ALIAS`: key alias that will be used to sign the app  
   `KEY_PASSWORD`: key password  
   **Warning**: keep this file safe and make sure nobody, except you, has access to it.
4. `$ cd CodeLoom`
5. Now you can open the project using **[Android Studio](https://developer.android.com/studio/)** or
   build manually from the command line: `./gradlew assembleRelease`.

#### Available flavors

* `gms`: A flavor used for publishing the app on Google Play
* `foss`: A flavor without closed-source libraries, used for publishing the app
  on GitHub [releases](https://github.com/wsnd/CodeLoom/releases)

## Translations

If you'd like to translate **CodeLoom** to a new language or make a translation correction,
please submit a pull request with the updated string resources
(`app/src/main/res/values-*/strings.xml`).

## Screenshots

<img src=".github/images/repository-screenshots.png">

## Attribution

This project is based on [Squircle CE](https://github.com/massivemadness/Squircle-CE)
by [massivemadness](https://github.com/massivemadness) and extends it with additional features.
The editor engine is built on [sora-editor](https://github.com/Rosemoe/sora-editor)
by [Rosemoe](https://github.com/Rosemoe).

## License

```
Copyright CodeLoom contributors.
Copyright Squircle CE contributors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

### Third-Party Licenses

This project uses several open source libraries:

- **Sora Editor** - Licensed under [LGPL v2.1](https://www.gnu.org/licenses/old-licenses/lgpl-2.1.html),
  included as a source-level git submodule with local modifications
- **Python Runtime** - Licensed under [PSF License](https://docs.python.org/3/license.html)
- And many others under Apache 2.0, MIT, BSD, and other licenses

For complete license information, please see:
- [NOTICE](NOTICE) - Attribution notices
- [THIRD-PARTY-LICENSES](THIRD-PARTY-LICENSES) - Complete third-party licenses
- [OPEN-SOURCE-LICENSES.md](OPEN-SOURCE-LICENSES.md) - User-friendly license summary
