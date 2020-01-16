<h1 align="center">enquirer</h1>

<p align="center">
	<a href="https://travis-ci.org/termapps/enquirer">
		<img src="https://img.shields.io/travis/termapps/enquirer.svg" alt="travis">
	</a>
</p>

<br>
<br>

<p align="center">
	<b>Command Line Utility for Stylish Interactive Prompts (like fzf but for all types)</b>
</p>

<br>

<p align="center">
	<sub>(Uses <a href="https://github.com/mitsuhiko/dialoguer">dialoguer</a> underneath)</sub>
</p>

<br>
<br>

## ❯ Getting started

Get started with Enquirer, the most powerful command line utility for creating interactive CLI prompts.

* [Install](#-install)
* [Usage](#-usage)
* [Prompts](#-prompts)
* [Changelog](#-changelog)
* [About](#-about)

## ❯ Install

`enquirer` is available on Linux, macOS

### With [Homebrew](https://brew.sh/)

```
$ brew tap "termapps/enquirer" "https://github.com/termapps/enquirer"
$ brew install enquirer
```

This is recommended way for installation on macOS since updating to the new version is easy.

### With [cargo](https://crates.io/)

```
$ cargo install enquirer
```

### As a single executable binary

Pre-built binary executables are available at [release page](https://github.com/termapps/enquirer/releases) for macOS (64bit), Linux (64bit, 32bit).
Download and unarchive the binary then put the executable in `$PATH`.

## ❯ Usage

### Command Line Utility

See [prompts][#-prompts] for information on subcommands.

```
enquirer 0.1.0
Command Line Utility for Stylish Interactive Prompts

USAGE:
    enquirer [FLAGS] <SUBCOMMAND>

FLAGS:
    -h, --help        Prints help information
        --no-color    Disable colors in the prompt
    -V, --version     Prints version information

SUBCOMMANDS:
    confirm    Prompt that returns `true` or `false`
    help       Prints this message or the help of the given subcommand(s)
```

### Library

If you want the dialoguer theme used in this tool you can add this package to your `Cargo.toml`

```rust
use dialoguer::Confirmation;
use enquirer::ColoredTheme;

fn main() {
    let prompt = Confirmation::with_theme(&ColoredTheme::default())
        .with_text("Do you want to continue?")
        .with_default(true);

    if prompt.interact()? {
        println!("Looks like you want to continue");
    } else {
        println!("nevermind then :(");
    }
}
```

## ❯ Prompts

## ❯ Changelog

Please see [CHANGELOG.md](CHANGELOG.md).

## ❯ About

### License
MIT/X11

### Bug Reports
Report [here](http://github.com/termapps/enquirer/issues).

### Creator
Pavan Kumar Sunkara (pavan.sss1991@gmail.com)

Follow me on [github](https://github.com/users/follow?target=pksunkara), [twitter](http://twitter.com/pksunkara)
