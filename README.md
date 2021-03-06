# Hack for Visual Studio Code

[![Build Status](https://travis-ci.org/PranayAgarwal/vscode-hack.svg?branch=master)](https://travis-ci.org/PranayAgarwal/vscode-hack)

This extension adds rich Hack language & HHVM support to Visual Studio Code. Visit [http://hacklang.org](http://hacklang.org) to get started with Hack.

It is published in the Visual Studio Marketplace [here](https://marketplace.visualstudio.com/items?itemName=pranayagarwal.vscode-hack). To install, search for "Hack" in the VS Code extensions tab or run the following command (⌘+P): ```ext install vscode-hack```.

**NOTE: This is a *very* early preview release.**

## Features

* Type Checking
* Autocomplete
* Hover Hints
* Document Symbol Outline
* Workspace Symbol Search
* Document Formatting
* Go To/Peek Definition
* Find All References
* Hack Coverage Check

![Hack for Visual Studio Code](https://cloud.githubusercontent.com/assets/341507/19377806/d7838da0-919d-11e6-9873-f5a6aa48aea4.gif)

## Requirements

This extension is supported on Linux and Mac OS X 10.10 onwards ([see HHVM compatibility](https://docs.hhvm.com/hhvm/installation/introduction)). The latest versions of Hack typechecking tools (`hh_client` and `hh_server`) are required on the local machine. The workspace should have a `.hhconfig` file at its root.    

## Configuration

This extension adds the following Visual Studio Code settings. These can be set in user preferences (⌘+,) or workspace settings (`.vscode/settings.json`).

* `hack.clientPath`: Absolute path to the `hh_client` executable. This can be left empty if `hh_client` is already in your environment $PATH. 

## Issues

Please file all bugs, issues, feature requests etc. at the [GitHub issues page](https://github.com/PranayAgarwal/vscode-hack/issues).

*Current known issues:*

- ([#1](https://github.com/PranayAgarwal/vscode-hack/issues/1), [Microsoft/vscode#10915](https://github.com/Microsoft/vscode/issues/10915)) The editor may not select the Hack language mode for `.php` files even if they start with ```<?hh```. To get around this, either manually select "Hack" as the file language from the selector on the bottom right of the screen, or configure your project workspace to open all `.php` files in Hack mode by adding the following to your workspace settings:

```json
    "files.associations": {
        "*.php": "hack"
    }
```
## Contributing

There are lots of ways to help! You can file new bugs and feature requests, or fix a pending one. To contribute to the source code, fork the repository on GitHub and create a pull request.

## Changelog

Please see the [list of recent releases and features added](https://github.com/PranayAgarwal/vscode-hack/releases). 

## License

The source code for this extension is available at [https://github.com/PranayAgarwal/vscode-hack](https://github.com/PranayAgarwal/vscode-hack) and is licenced under the [MIT license](LICENSE.md).
