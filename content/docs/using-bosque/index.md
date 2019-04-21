---
title: "Using Bosque"
date: 2019-04-21T11:46:37+07:00
weight: 2
---

The current concentrate of the Bosque language is core design. Because of this there is limited support for development/compilation as well as no support for packaging, deployment, lifecycle management, etc.

## Requirements

### Windows

In order to build the language for Windows the following are needed:

* The LTS version of node.js for Windows (x64)

* Typescript (install with: ```npm i typescript -g```)

### Build & Test

The ```ref_impl``` directory contains the reference implementation parser, type checker, interpreter, and command line runner. In this directory, build and test the Bosque reference implementation with:
```
npm install && npm run-script build && npm test
```

### Command Line Execution

The ```ref_impl``` directory contains a simple command line runner for standalone Bosque (```.bsq```) files. These files must have a single ```entrypoint``` function called ```main()```. The code in the file can be parsed, type checked, and executed with:

```
node bin/test/app_runner.js FILE.bsq
```

### Visual Studio Code Integration

This repository provides basic Visual Studio Code IDE support for the Bosque language (currently limited to syntax and brace highlighting). The installation requires manually copying the full ```bosque-language-tools/``` folder into your user ```.vscode/extensions/``` directory and restarting VSCode.
