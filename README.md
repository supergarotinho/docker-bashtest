<h1 align="center">Docker bash tests &nbsp; <a href="https://twitter.com/intent/tweet?text=Execute%20and%20generate%20bash%20testing%20report%20with%20supergarotinho%2Fbashtest%20image!&amp;url=https://www.gruponeuro.com.br&amp;via=supergarotinho&amp;hashtags=docker,bash,test,testing,report,coverage,shunit2,kcov" rel="nofollow"><img src="https://camo.githubusercontent.com/83d4084f7b71558e33b08844da5c773a8657e271/68747470733a2f2f696d672e736869656c64732e696f2f747769747465722f75726c2f687474702f736869656c64732e696f2e7376673f7374796c653d736f6369616c" alt="Tweet" data-canonical-src="https://img.shields.io/twitter/url/http/shields.io.svg?style=social" style="max-width:100%;"></a>
</h1>
<div align="center">
  <strong>Fun programming with bash and docker</strong>
</div>
<div align="center">
  Image with <code>kcov</code> and <code>shunit2</code> to execute tests and generate a code coverage report.
</div>

<br />

<div align="center">
  <!-- Price -->
  <a href="https://github.com/supergarotinho/docker-bashtest/blob/master/LICENSE">
    <img src="https://img.shields.io/badge/price-FREE-0098f7.svg"
      alt="Price" />
  </a>
  <!-- Build Status -->
  <a href="https://hub.docker.com/r/supergarotinho/bashtest/">
    <img src="https://dockerbuildbadges.quelltext.eu/status.svg?organization=supergarotinho&repository=bashtest"
      alt="Build Status" />
  </a>
  <!-- Docker Stars -->
  <a href="https://hub.docker.com/r/supergarotinho/bashtest/">
    <img src="https://img.shields.io/docker/stars/supergarotinho/bashtest.svg"
      alt="Docker Stars" />
  </a>
  <!-- Docker Pulls -->
  <a href="https://hub.docker.com/r/supergarotinho/bashtest/">
    <img src="https://img.shields.io/docker/pulls/supergarotinho/bashtest.svg"
      alt="Docker Pulls" />
  </a>
  <!-- License: BSD-3 -->
  <a href="https://github.com/supergarotinho/docker-bashtest/blob/master/LICENSE">
    <img src="https://img.shields.io/badge/license-BSD3-blue.svg"
      alt="License: BSD-3" />
  </a>
  <!-- Contributions welcome -->
  <img src="https://img.shields.io/badge/contributions-welcome-orange.svg"
    alt="Contributions welcome" />
</div>

<br/>

## Table of contents

- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
- [Built With](#built-with)
- [Authors](#authors)
- [Community](#community)
- [License](#license)

## Features

* **Shunit2:** Has shunit2 installed
* **Kcov:** has kcov installed

## Getting Started

You must mount the source code and execute the test script inside the image with kcov command. The example is bellow.

There is a repository with a example of a bash script using this image at: https://github.com/supergarotinho/bashtest-example

Example of use:

```bash
docker run --rm \
  --security-opt seccomp=unconfined \
  -v "$(pwd)":/source \
  -e "TERM=xterm-256color" supergarotinho/bashtest kcov --exclude-path=/root/shunit2 ./coverage ./test/unit-test.sh
```

### Prerequisites

* Docker installed

## Built With

* [Shunit2](https://github.com/kward/shunit2) - The bash testing framework
* [Kcov](https://github.com/SimonKagstrom/kcov) - Code coverage tool for compiled programs, Python and Bash which uses debugging information to collect and report data without special compilation options

## Authors

* **Anderson Santos** - *Initial work* - [supergarotinho](https://github.com/supergarotinho)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the BSD-3 License - see the [LICENSE.md](LICENSE.md) file for details
