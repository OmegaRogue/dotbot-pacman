# Dotbot yay Plugin

For use with [dotbot](https://github.com/anishathalye/dotbot),
this plugin allows one to easily install or upgrade a list of pacman packages.

This plugin is a port of [dotbot-yay](https://github.com/OxSon/dotbot-yay) for use with `pacman`. Basically the same thing with a `:%s/yay/pacman` command ran, plus a couple other relevant changes.

## Usage

It's easiest to track this plugin in your dotfiles repo:

```bash
git submodule add https://github.com/omegarogue/dotbot-pacman
```

The original author also recommends having your yay list in a separate file
since dotbot will need root privileges in order to use the plugin.

If you use the default install script provided by [dotbot](https://github.com/anishathalye/dotbot), using the plugin will look like this:

```bash
./dotbot/bin/dotbot -p dotbot-pacman/pacman.py -c packages.conf.yaml
```

Using the `install` script provided by this repo, using the plugin will look like this:
```bash
./install packages
```

Example for `packages.conf.yaml`:

```yaml
- pacman:
  - vim
  - zsh
  - tldr
```
