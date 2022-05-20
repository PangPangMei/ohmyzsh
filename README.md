<p align="center"><img src="https://ohmyzsh.s3.amazonaws.com/omz-ansi-github.png" alt="Oh My Zsh"></p>

Oh My Zsh is an open source, community-driven framework for managing your [zsh](https://www.zsh.org/) configuration.

Sounds boring. Let's try again.

**Oh My Zsh will not make you a 10x developer...but you may feel like one.**

Once installed, your terminal shell will become the talk of the town _or your money back!_ With each keystroke in your command prompt, you'll take advantage of the hundreds of powerful plugins and beautiful themes. Strangers will come up to you in cafés and ask you, _"that is amazing! are you some sort of genius?"_

Finally, you'll begin to get the sort of attention that you have always felt you deserved. ...or maybe you'll use the time that you're saving to start flossing more often. 😬

To learn more, visit [ohmyz.sh](https://ohmyz.sh), follow [@ohmyzsh](https://twitter.com/ohmyzsh) on Twitter, and join us on [Discord](https://discord.gg/ohmyzsh).

[![CI](https://github.com/ohmyzsh/ohmyzsh/workflows/CI/badge.svg)](https://github.com/ohmyzsh/ohmyzsh/actions?query=workflow%3ACI)
[![Follow @ohmyzsh](https://img.shields.io/twitter/follow/ohmyzsh?label=Follow+@ohmyzsh&style=flat)](https://twitter.com/intent/follow?screen_name=ohmyzsh)
[![Discord server](https://img.shields.io/discord/642496866407284746)](https://discord.gg/ohmyzsh)
[![Gitpod ready](https://img.shields.io/badge/Gitpod-ready-blue?logo=gitpod)](https://gitpod.io/#https://github.com/ohmyzsh/ohmyzsh)
[![huntr.dev](https://cdn.huntr.dev/huntr_security_badge_mono.svg)](https://huntr.dev/bounties/disclose/?utm_campaign=ohmyzsh%2Fohmyzsh&utm_medium=social&utm_source=github&target=https%3A%2F%2Fgithub.com%2Fohmyzsh%2Fohmyzsh)

<details>
<summary>Table of Contents</summary>

- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Basic Installation](#basic-installation)
    - [Manual inspection](#manual-inspection)
- [Using Oh My Zsh](#using-oh-my-zsh)
  - [Plugins](#plugins)
    - [Enabling Plugins](#enabling-plugins)
    - [Using Plugins](#using-plugins)
  - [Themes](#themes)
    - [Selecting a Theme](#selecting-a-theme)
  - [FAQ](#faq)
- [Advanced Topics](#advanced-topics)
  - [Advanced Installation](#advanced-installation)
    - [Custom Directory](#custom-directory)
    - [Unattended install](#unattended-install)
    - [Installing from a forked repository](#installing-from-a-forked-repository)
    - [Manual Installation](#manual-installation)
  - [Installation Problems](#installation-problems)
  - [Custom Plugins and Themes](#custom-plugins-and-themes)
- [Getting Updates](#getting-updates)
  - [Manual Updates](#manual-updates)
- [Uninstalling Oh My Zsh](#uninstalling-oh-my-zsh)
- [How do I contribute to Oh My Zsh?](#how-do-i-contribute-to-oh-my-zsh)
  - [Do NOT send us themes](#do-not-send-us-themes)
- [Contributors](#contributors)
- [Follow Us](#follow-us)
- [Merchandise](#merchandise)
- [License](#license)
- [About Planet Argon](#about-planet-argon)

</details>

## Getting Started

### Prerequisites

- A Unix-like operating system: macOS, Linux, BSD. On Windows: WSL2 is preferred, but cygwin or msys also mostly work.
- [Zsh](https://www.zsh.org) should be installed (v4.3.9 or more recent is fine but we prefer 5.0.8 and newer). If not pre-installed (run `zsh --version` to confirm), check the following wiki instructions here: [Installing ZSH](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
- `curl` or `wget` should be installed
- `git` should be installed (recommended v2.4.11 or higher)

### Basic Installation

Oh My Zsh is installed by running one of the following commands in your terminal. You can install this via the command-line with either `curl`, `wget` or another similar tool.

| Method    | Command                                                                                           |
| :-------- | :------------------------------------------------------------------------------------------------ |
| **curl**  | `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |
| **wget**  | `sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`   |
| **fetch** | `sh -c "$(fetch -o - https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |

_Note that any previous `.zshrc` will be renamed to `.zshrc.pre-oh-my-zsh`. After installation, you can move the configuration you want to preserve into the new `.zshrc`._

#### Manual inspection

It's a good idea to inspect the install script from projects you don't yet know. You can do
that by downloading the install script first, looking through it so everything looks normal,
then running it:

```sh
wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
sh install.sh
```

## Using Oh My Zsh

### Plugins

Oh My Zsh comes with a shitload of plugins for you to take advantage of. You can take a look in the [plugins](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins) directory and/or the [wiki](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins) to see what's currently available.

#### Enabling Plugins

Once you spot a plugin (or several) that you'd like to use with Oh My Zsh, you'll need to enable them in the `.zshrc` file. You'll find the zshrc file in your `$HOME` directory. Open it with your favorite text editor and you'll see a spot to list all the plugins you want to load.

```sh
vi ~/.zshrc
```

For example, this might begin to look like this:

```sh
plugins=(
  git
  bundler
  dotenv
  macos
  rake
  rbenv
  ruby
)
```

_Note that the plugins are separated by whitespace (spaces, tabs, new lines...). **Do not** use commas between them or it will break._

#### Using Plugins

Each built-in plugin includes a **README**, documenting it. This README should show the aliases (if the plugin adds any) and extra goodies that are included in that particular plugin.

### Themes

We'll admit it. Early in the Oh My Zsh world, we may have gotten a bit too theme happy. We have over one hundred and fifty themes now bundled. Most of them have [screenshots](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes) on the wiki (We are working on updating this!). Check them out!

#### Selecting a Theme

_Robby's theme is the default one. It's not the fanciest one. It's not the simplest one. It's just the right one (for him)._

Once you find a theme that you'd like to use, you will need to edit the `~/.zshrc` file. You'll see an environment variable (all caps) in there that looks like:

```sh
ZSH_THEME="robbyrussell"
```

To use a different theme, simply change the value to match the name of your desired theme. For example:

```sh
ZSH_THEME="agnoster" # (this is one of the fancy ones)
# see https://github.com/ohmyzsh/ohmyzsh/wiki/Themes#agnoster
```

_Note: many themes require installing a [Powerline Font](https://github.com/powerline/fonts) or a [Nerd Font](https://github.com/ryanoasis/nerd-fonts) in order to render properly. Without them, these themes will render [weird prompt symbols](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ#i-have-a-weird-character-in-my-prompt)_

Open up a new terminal window and your prompt should look something like this:

![Agnoster theme](https://cloud.githubusercontent.com/assets/2618447/6316862/70f58fb6-ba03-11e4-82c9-c083bf9a6574.png)

In case you did not find a suitable theme for your needs, please have a look at the wiki for [more of them](https://github.com/ohmyzsh/ohmyzsh/wiki/External-themes).

If you're feeling feisty, you can let the computer select one randomly for you each time you open a new terminal window.

```sh
ZSH_THEME="random" # (...please let it be pie... please be some pie..)
```

And if you want to pick random theme from a list of your favorite themes:

```sh
ZSH_THEME_RANDOM_CANDIDATES=(
  "robbyrussell"
  "agnoster"
)
```

If you only know which themes you don't like, you can add them similarly to an ignored list:

```sh
ZSH_THEME_RANDOM_IGNORED=(pygmalion tjkirch_mod)
```

### FAQ

If you have some more questions or issues, you might find a solution in our [FAQ](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ).

## Advanced Topics

If you're the type that likes to get their hands dirty, these sections might resonate.

### Advanced Installation

Some users may want to manually install Oh My Zsh, or change the default path or other settings that
the installer accepts (these settings are also documented at the top of the install script).

#### Custom Directory

The default location is `~/.oh-my-zsh` (hidden in your home directory, you can access it with `cd ~/.oh-my-zsh`)

If you'd like to change the install directory with the `ZSH` environment variable, either by running
`export ZSH=/your/path` before installing, or by setting it before the end of the install pipeline
like this:

```sh
ZSH="$HOME/.dotfiles/oh-my-zsh" sh install.sh
```

#### Unattended install

If you're running the Oh My Zsh install script as part of an automated install, you can pass the `--unattended`
flag to the `install.sh` script. This will have the effect of not trying to change
the default shell, and it also won't run `zsh` when the installation has finished.

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" "" --unattended
```

#### Installing from a forked repository

The install script also accepts these variables to allow installation of a different repository:

- `REPO` (default: `ohmyzsh/ohmyzsh`): this takes the form of `owner/repository`. If you set
  this variable, the installer will look for a repository at `https://github.com/{owner}/{repository}`.

- `REMOTE` (default: `https://github.com/${REPO}.git`): this is the full URL of the git repository
  clone. You can use this setting if you want to install from a fork that is not on GitHub (GitLab,
  Bitbucket...) or if you want to clone with SSH instead of HTTPS (`git@github.com:user/project.git`).

  _NOTE: it's incompatible with setting the `REPO` variable. This setting will take precedence._

- `BRANCH` (default: `master`): you can use this setting if you want to change the default branch to be
  checked out when cloning the repository. This might be useful for testing a Pull Request, or if you
  want to use a branch other than `master`.

For example:

```sh
REPO=apjanke/oh-my-zsh BRANCH=edge sh install.sh
```

#### Manual Installation

##### 1. Clone the repository <!-- omit in toc -->

```sh
git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.oh-my-zsh
```

##### 2. _Optionally_, backup your existing `~/.zshrc` file <!-- omit in toc -->

```sh
cp ~/.zshrc ~/.zshrc.orig
```

##### 3. Create a new zsh configuration file <!-- omit in toc -->

You can create a new zsh config file by copying the template that we have included for you.

```sh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
```

##### 4. Change your default shell <!-- omit in toc -->

```sh
chsh -s $(which zsh)
```

You must log out from your user session and log back in to see this change.

##### 5. Initialize your new zsh configuration <!-- omit in toc -->

Once you open up a new terminal window, it should load zsh with Oh My Zsh's configuration.

### Installation Problems

If you have any hiccups installing, here are a few common fixes.

- You _might_ need to modify your `PATH` in `~/.zshrc` if you're not able to find some commands after switching to `oh-my-zsh`.
- If you installed manually or changed the install location, check the `ZSH` environment variable in `~/.zshrc`.

### Custom Plugins and Themes

If you want to override any of the default behaviors, just add a new file (ending in `.zsh`) in the `custom/` directory.

If you have many functions that go well together, you can put them as a `XYZ.plugin.zsh` file in the `custom/plugins/` directory and then enable this plugin.

If you would like to override the functionality of a plugin distributed with Oh My Zsh, create a plugin of the same name in the `custom/plugins/` directory and it will be loaded instead of the one in `plugins/`.

## Getting Updates

By default, you will be prompted to check for updates every 2 weeks. You can choose other update modes by adding a line to your `~/.zshrc` file, **before Oh My Zsh is loaded**:

1. Automatic update without confirmation prompt:

   ```sh
   zstyle ':omz:update' mode auto
   ```

2. Just offer a reminder every few days, if there are updates available:

   ```sh
   zstyle ':omz:update' mode reminder
   ```

3. To disable automatic updates entirely:

   ```sh
   zstyle ':omz:update' mode disabled
   ```

NOTE: you can control how often Oh My Zsh checks for updates with the following setting:

```sh
# This will check for updates every 7 days
zstyle ':omz:update' frequency 7
# This will check for updates every time you open the terminal (not recommended)
zstyle ':omz:update' frequency 0
```

### Manual Updates

If you'd like to update at any point in time (maybe someone just released a new plugin and you don't want to wait a week?) you just need to run:

```sh
omz update
```

Magic! 🎉

## Uninstalling Oh My Zsh

Oh My Zsh isn't for everyone. We'll miss you, but we want to make this an easy breakup.

If you want to uninstall `oh-my-zsh`, just run `uninstall_oh_my_zsh` from the command-line. It will remove itself and revert your previous `bash` or `zsh` configuration.

## How do I contribute to Oh My Zsh?

Before you participate in our delightful community, please read the [code of conduct](CODE_OF_CONDUCT.md).

I'm far from being a [Zsh](https://www.zsh.org/) expert and suspect there are many ways to improve – if you have ideas on how to make the configuration easier to maintain (and faster), don't hesitate to fork and send pull requests!

We also need people to test out pull requests. So take a look through [the open issues](https://github.com/ohmyzsh/ohmyzsh/issues) and help where you can.

See [Contributing](CONTRIBUTING.md) for more details.

### Do NOT send us themes

We have (more than) enough themes for the time being. Please add your theme to the [external themes](https://github.com/ohmyzsh/ohmyzsh/wiki/External-themes) wiki page.

## Contributors

Oh My Zsh has a vibrant community of happy users and delightful contributors. Without all the time and help from our contributors, it wouldn't be so awesome.

Thank you so much!

## Follow Us

We're on social media:

- [@ohmyzsh](https://twitter.com/ohmyzsh) on Twitter. You should follow it.
- [Facebook](https://www.facebook.com/Oh-My-Zsh-296616263819290/) poke us.
- [Instagram](https://www.instagram.com/_ohmyzsh/) tag us in your post showing Oh My Zsh!
- [Discord](https://discord.gg/ohmyzsh) to chat with us!

## Merchandise

We have [stickers, shirts, and coffee mugs available](https://shop.planetargon.com/collections/oh-my-zsh?utm_source=github) for you to show off your love of Oh My Zsh. Again, you will become the talk of the town!

## License

Oh My Zsh is released under the [MIT license](LICENSE.txt).

## About Planet Argon

![Planet Argon](https://pa-github-assets.s3.amazonaws.com/PARGON_logo_digital_COL-small.jpg)

Oh My Zsh was started by the team at [Planet Argon](https://www.planetargon.com/?utm_source=github), a [Ruby on Rails development agency](https://www.planetargon.com/skills/ruby-on-rails-development?utm_source=github). Check out our [other open source projects](https://www.planetargon.com/open-source?utm_source=github).


Ubuntu美化——安装Oh-My-Zsh
一、安装zsh
安装zsh
复制代码
1
BASH
sudo apt-get install zsh
把默认的Shell改成zsh
注意：不要使用sudo。
复制代码
1
LANGUAGE-BASH
chsh -s /bin/zsh
配置密码文件，解决chsh: PAM认证失败的问题
编辑passwd文件
复制代码
1
LANGUAGE-BASH
sudo vim /etc/passwd
把第一行的/bin/bash改成/bin/zsh，这个是root用户的。
复制代码
1
BASH
root:x:0:0:root:/root:/bin/zsh
把用户的bash也改为zsh，以下是我的。
复制代码
1
BASH
langkye:x:1000:1000:langkye,,,:/home/langkye:/usr/bin/zsh
4、安装Git，如果已经安装，自行跳过

复制代码
1
LANGUAGE-CSHARP
sudo apt-get install git
二、安装 Oh my zsh
zsh的强大令人敬畏，但是由于它配置复杂，很多人对它望而却步，而oh my zsh的诞生正好从某种角度上解决了此问题。
zsh在github上的repo地址为 robbyrussell/oh-my-zsh

其提供了一键安装工具，按照其说明，仅需运行如下命令。
2.1使用wget安装
推荐使用wget

复制代码
1
BASH
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
码云地址加速
复制代码
1
2
BASH
# gitee 源
sh -c "$(wget https://gitee.com/mirrors/oh-my-zsh/raw/master/tools/install.sh -O -)"
2.2使用curl来安装
复制代码
1
BASH
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
码云地址加速
复制代码
1
2
BASH
# gitee 源
sh -c "$(curl -fsSL wget https://gitee.com/mirrors/oh-my-zsh/raw/master/tools/install.sh)"
接下来静静等待安装完毕～

三、美化Oh my zsh
3.1配置主题
Oh my zsh自带了非常实用的主题特性，其自身也提供了诸多主题以供切换。
需要注意的是，有些个别的主题需要安装特殊的字体。

官方对主题的介绍以及已提交的主题列表在这里 robbyrussell/oh-my-zsh。

这里以agnoster这个主题为例

因为zsh已自带此主题，主题文件已存在于~/.oh_my_zsh/themes文件夹下，故可直接使用。如果你需要安装其他并非自带的主题的话，请将主题文件拷贝至此文件夹。

首先切换到当前账户主目录，编辑.zshrc文件。
找到ZSH_THEME这一项，将它的值改成agnoster即可完成对此主题的切换，其他主题如法炮制。
复制代码
1
BASH
vim .zshrc
默认值：ZSH_THEME="robbyrussell"

编辑完毕后，重载该配置文件，无需重启。
复制代码
1
BASH
source .zshrc
3.2安装autojump
autojump为Oh my zsh的一款自动跳转插件。官网：https://github.com/wting/autojump

安装
复制代码
1
LANGUAGE-CSHARP
sudo apt-get install autojump
配置

复制代码
1
BASH
vim .zshrc
在最后一行加入，注意点后面是一个空格
复制代码
1
BASH
. /usr/share/autojump/autojump.sh
如需详细配置，参考【配置教程】：cat /usr/share/doc/autojump/README.Debian。

重载配置文件

复制代码
1
LANGUAGE-BASH
source ~/.zshrc
3.3安装语法高亮插件
官网：https://github.com/zsh-users/zsh-syntax-highlighting

安装zsh-syntax-highlighting插件
复制代码
1
2
LANGUAGE-BASH
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
echo "source ${(q-)PWD}/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ${ZDOTDIR:-$HOME}/.zshrc
重载配置文件
复制代码
1
LANGUAGE-BASH
source ~/.zshrc
3.4安装语法历史记录插件
官网：https://github.com/zsh-users/zsh-autosuggestions

安装zsh-autosuggestions
复制代码
1
LANGUAGE-BASH
git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
编辑.zshrc，添加插件
复制代码
1
LANGUAGE-BASH
vim ~/.zshrc
将zsh-autosuggestions添加到plugins()，示例：
复制代码
1
2
3
4
5
6
7
BASH
# 原来：
# plugins(git)
# 追加：
pulguns(
      git
      zsh-autosuggestions
)
在末尾添加一行：
复制代码
1
BASH
source $ZSH_CUSTOM/plugins/zsh-autosuggestions/zsh-autosuggestions.zsh
重载配置文件
复制代码
1
BASH
source ~/.zshrc
3.4配置主题
在3.1已经配置过，如果不需要换，可忽略。

官方主题参考：https://github.com/robbyrussell/oh-my-zsh/wiki/External-themes

编辑配置文件
复制代码
1
LANGUAGE-BASH
sudo vim ~/.zshrc
找到ZSH_THEME="robbyrussell"，修改为：ZSH_THEME="ys"；

重载配置文件
复制代码
1
LANGUAGE-BASH
source ~/.zshrc