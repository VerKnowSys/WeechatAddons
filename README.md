# WeeChatAddons

This repository contains cherry picked plugins, themes and other configuration goodies for best [Slack](https://slack.com/) experience under [WeeChat](https://weechat.org/) client.


## Authors:


* Sébastien Helleu:
    - WeeChat lead developer,

* Ryan Huber:
    - wee_slack.py lead developer,

* Daniel (dmilith) Dettlaff:
    - prebuilt software preparation,
    - picked a few mandatory plugins,
    - prepared default configuration,


## Requirements:

* Modern terminal with full UTF-8 support (iTerm, Terminal.app, Konsole, Gnome-terminal, urxvt, …).

* Weechat 2.2 (prebuilt version for macOS 10.11+ [is available here](http://software.verknowsys.com/binary/Darwin-10.11-x86_64/Weechat-2.2-Darwin-10.11-x86_64.txz)).

* Python 2.x (already installed under macOS).

* Perl 5.x (already installed under macOS).


## Additional plugin dependencies:

### wee_slack.py:

> NOTE: wee_slack.py plugin operates on Slack websockets directly (exactly as "regular Slack web-client" does), hence additional pip extension has to be installed:

`pip install websocket-client` (you may need root access)


### notification_center.py:

> NOTE: notification_center.py plugin is macOS-only - for other notification systems - seek for compatible "notify" plugin here: https://weechat.org/scripts/). Additional pip extension has to be installed:

`pip install pync` (you may need root access)


## Installation:

* Copy `plugins/*.pl` files to: `~/.weechat/perl/autoload`

* Copy `plugins/*.py` files to: `~/.weechat/python/autoload`

* Copy `themes/*` files to: `~/.weechat/themes`. If you don't like `flashcode.theme` (my fav), you can find more themes here: https://weechat.org/themes/.

* Copy `config/*.conf` files to `~/.weechat/`

* Restart `weechat` :)


## Run the thing:

* Start `weechat`

* Type `/slack register` in WeeChat - for each your Slack organization. Follow displayed steps.

* Type `/slack register URI-CODE-FROM-PARAMS` to finish configuration.

* Type `/save` to make WeeChat configuration persistent.

* That's all! It should work.

> NOTE: Full mouse support is enabled for WeeChat!
>       You can use LMB to switch channels/queries.
>       RMB can be used on special elements (like settings) -
>       to quickly copy+paste "value under mouse cursor", to the input bar.
>       If you need to open a link (at least in Terminal.app) - you can use `fn` key
>       and RMB on URI, to open it (or use `meta-l` keystroke to trigger window "bare mode". In bare window, you can select link - like in any other application).
>       Mouse scrolling is also fully supported for all windows and users list.
>       If you find mouse support iritating, type `/mouse disable` in WeeChat.


## Default (and also most useful) keystrokes:

* `meta-a` or `meta-j` - jump to next window with activity.

* `ctrl-n` - switch to next window

* `ctrl-p` - switch to previous window

* `meta-1…0` - switch to window with number 1..10

* `meta-q…p` - switch to window with number 11..20

* `meta-d` - close current window

* `meta-l` - trigger bare(raw) mode for current window (mouse triggers are disabled for bare window)


## Useful commands:

* `/buffer *NUM` - switch to window buffer number "NUM"

* `/layout store YOURNAME` - makes current layout of WeeChat's buffer windows persistent.


## Main resources:

* WeeChat - [project page](https://weechat.org/)

* WeeChat Scripts (plugins) - [scripts page](https://weechat.org/scripts/)

* wee_slack.py - [project page](https://github.com/wee-slack/wee-slack)
