# WeeChatAddons

This repository contains cherry picked scripts, themes and other configuration goodies for best [Slack](https://slack.com/) experience under [WeeChat](https://weechat.org/) client.


## Authors:


* Sébastien Helleu:
    - WeeChat lead developer,
    - theme.py lead developer,

* Ryan Huber:
    - wee_slack.py lead developer,

* Sindre Sorhus:
    - notification_center.py lead developer,

* Stefan Wold:
    - weemoticons.py lead developer,

* Nei:
    - multiline.pl lead developer,

* nils_2:
    - histman.py lead developer,

* Daniel (dmilith) Dettlaff:
    - prebuilt software preparation,
    - picked a few mandatory scripts,
    - prepared default configuration,


## But… why?

WeeChat connected to 6 distinct Slack groups uses `80-120` MiB of RAM with it's "background messages prefetch" feature enabled! Try that with default Slack web client. ;)


## Requirements:

* Modern terminal with full UTF-8 support (iTerm, Terminal.app, Konsole, Gnome-terminal, urxvt, …).

* Weechat 2.2 (prebuilt version for macOS 10.11+ [is available here](http://software.verknowsys.com/binary/Darwin-10.11-x86_64/Weechat-2.2-Darwin-10.11-x86_64.txz), as a [Sofin](https://github.com/VerKnowSys/sofin) bundle. Bundle can also be manually unpacked to: `/Software/Weechat`. To start it after unpack, try: `/Software/Weechat/exports/weechat`).

* Python 2.x (already installed under macOS).

* Perl 5.x (already installed under macOS).


## Additional scripts dependencies:

### wee_slack.py:

> NOTE: wee_slack.py plugin operates on Slack websockets directly (exactly as "regular Slack web-client" does), hence additional pip extension has to be installed:

`pip install websocket-client` (you may need root access)


### notification_center.py:

> NOTE: notification_center.py plugin is macOS-only - for other notification systems - seek for compatible "notify" plugin here: https://weechat.org/scripts/). Additional pip extension has to be installed:

`pip install pync` (you may need root access)


## Installation:

* Install `weechat` client software.

* Run `weechat` once (to init your `~/.weechat` directory), then quit it by typing `/quit`.

* Copy `scripts/*.pl` files to: `~/.weechat/perl/autoload`

* Copy `scripts/*.py` files to: `~/.weechat/python/autoload`

* Copy `themes/*` files to: `~/.weechat/themes`. If you don't like `flashcode.theme` (my fav), you can find more themes here: https://weechat.org/themes/.

* Copy `config/*.conf` files to `~/.weechat/`

* Start `weechat` and enjoy! :)


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

* `fn` - keep pressed to enable mouse select (under Terminal.app, may be also `shift` or `alt`)

* `meta-a` or `meta-j` - jump to next window with activity.

* `ctrl-n` - switch to next window.

* `ctrl-p` - switch to previous window.

* `meta-1…0` - switch to window with number 1..10

* `meta-q…p` - switch to window with number 11..20

* `meta-d` - close current window.

* `meta-l` - trigger bare(raw) mode for current window (mouse triggers are disabled for bare window).


## Useful commands:

* `s/inztaWler/installer/` - fix "the typo" in your most recent message.

* `2s///` - delete your second last entered message.

* `/set keyword` - shows all variables that have "keyword" in their name/path. For example: `/set timeout` - shows all available timeout variables. `/set slack` - shows all Slack specific settings and so on…

* `/set some.variable.path "some-value"` - sets given variable with given value. Example: `/set plugins.var.python.slack.background_load_all_history "true"`.

* `/buffer *NUM` - switch to window buffer number "NUM".

* `/layout store YOURNAME` - makes current layout of WeeChat's buffer windows persistent.


## Adding own key binds:

* `/key bind meta-j /input jump_smart` - binds `meta-j` keystroke to WeeChat's /input command to jump to next active window buffer.


## Adding own commands (a.k.a. aliases):

* `/alias add shrug /slack slash /shrug` - will define `/shrug` command for WeeChat that's calling Slack feature ("slash" allows direct access to Slack-specific commands).


## Adding Slack "reaction" - reply on `Nth` last message in WeeChat's current window (N=1 is default and can be ommited). For example:

* `+:wink:` - set "wink" on last message in current window

* `5+:muscle:` - set "muscle" reaction on 5th message from current

> NOTE: More examples available on: [wee-slack github page](https://github.com/wee-slack/wee-slack)


## Say cheese!


> Channel `#general` of `Rust-Slack` group from `WeeChat`:

![Rust-lang Slack group from WeeChat](http://s.verknowsys.com/27348367e1d139fb8be585fac2c19c8f.png)



## Main resources:

* WeeChat - [project page](https://weechat.org/)

* WeeChat Scripts - [scripts page](https://weechat.org/scripts/)

* wee_slack.py - [project page](https://github.com/wee-slack/wee-slack)
