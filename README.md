[![Build Status](https://travis-ci.org/lee-dohm/auto-copyright.svg?branch=master)](https://travis-ci.org/lee-dohm/auto-copyright)

# Auto-Copyright

Inserts or updates a copyright notice.

## Installation

This package can be installed from the Settings View by searching for `auto-copyright` or can be installed from the command line by using the command: `apm install auto-copyright`.

## Usage

### Insert

The `auto-copyright:insert` command adds the configured copyright text with the current year and configured owner text as a comment at the top of the file. The default copyright text looks like this:

```coffee
#
# Copyright (c) 2014 by Placeholder Corporation. All Rights Reserved.
#
```

It can be configured to say as much or as little as you want, though.

### Update

When you execute the `auto-copyright:update` command, it updates the copyright year in a standard format by adding the current year to the list of years and compacting it in the following ways:

* Disjoint years are separated by commas: 2000, 2005 and 2010 are represented as `2000, 2005, 2010`
* Years in a series are represented by the start and end years separated by a hyphen: 2001, 2002 and 2003 are represented as `2001-2003`
* Mixing and matching works too: 2001, 2002, 2003, 2005 and 2010 are represented as `2001-2003, 2005, 2010`

## Configuration

Auto Copyright supports the following configuration settings:

* `auto-copyright.buffer` &mdash; Number of blank commented lines before and after the copyright text. (Defaults to: `1`)
* `auto-copyright.owner` &mdash; Owner name to use when creating the copyright text.
* `auto-copyright.template` &mdash; Copyright template to follow. `%y` will be replaced with the current year. `%o` will be replaced with the owner name. (Defaults to: `Copyright (c) %y by %o. All Rights Reserved.`)

### Commands

* `auto-copyright:insert` &mdash; Inserts the copyright text at the top of the file in the active editor
* `auto-copyright:update` &mdash; Updates the year range of the copyright text at the top of the file, if it exists

### Keybindings

No keybindings are assigned by default.

## Copyright

Copyright &copy; 2014 [Lee Dohm](http://www.lee-dohm.com), [Lifted Studios](http://www.liftedstudios.com). See [LICENSE](LICENSE.md) for details.
