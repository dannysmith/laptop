# Sparta Global Laptop Config

This script is designed to install and configure Sparta student and trainer macOS machines.

## Steps to configure a new Mac

1. Initial macOS Setup Wizard (Laptop name, WiFi etc). Admin staff will provide the username and password to use when configuring this part.
2. Run `xcode-select --install` to install the Command Line tools.
3. Run install script:

```shell
git clone https://github.com/spartaglobal/laptop.git $HOME/laptop
cd $HOME/laptop
$HOME/laptop/install
```

Type the **password you use to login** when prompted.

### Setting your terminal profile and font

Open the preferences of Terminal.app. If SpartaPro doesn't appear in the list on the left, click the cog and choose **Import**. Choose the SpartaPro theme, which should be at `~/SpartaPro.terminal`. Click the **Default** button to set it as your default. Finally, change the font to `Inconsolata 16pt`.

![Image](https://raw.githubusercontent.com/spartaglobal/laptop/master/assets/terminal.png)

## Resetting a laptop

To reset a laptop after a course, run the reset script with:

```shell
git clone https://github.com/spartaglobal/laptop.git $HOME/laptop
cd $HOME/laptop
$HOME/laptop/reset
```

Type the **password you use to login** when prompted.

**THIS IS A DESTRUCTIVE SCRIPT AND WILL REMOVE APPLICATIONS, FILES AND SETTINGS. THERE IS NO WAY TO UNDO ITS ACTIONS**

## Running in a single command

If you need to script this process, there are two small scripts provided: `remote-install` and `remote-reset`. They _should_ clone down the repo and execute it in a single command, but haven't been fully tested yet.

To do so, run:

```shell
`cd ~; bash <(curl -s https://raw.githubusercontent.com/spartaglobal/laptop/master/remote-install)`
```

or

```shell
`cd ~; bash <(curl -s https://raw.githubusercontent.com/spartaglobal/laptop/master/remote-reset)`
```

## Inspiration

Bits of this script were borrowed from all over the internet, but in particular:

- <https://github.com/attack/laptop>
- <https://github.com/thoughtbot/laptop/>

Initially built by [@dannysmith](http://github.com/dannysmith).
