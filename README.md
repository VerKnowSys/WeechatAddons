## Requirements:

* Modern terminal with full UTF-8 support (iTerm, Terminal.app, Konsole, Gnome-terminal, urxvt, …).
* Weechat 2.2 (prebuilt version for macOS 10.11+ [is available here](http://software.verknowsys.com/binary/Darwin-10.11-x86_64/Weechat-2.2-Darwin-10.11-x86_64.txz)).
* Python 2.x (already installed under macOS).
* Perl 5.x (already installed under macOS).


### Additional plugin dependencies:

#### wee_slack.py:

> NOTE: wee_slack.py plugin operates on Slack websockets directly (exactly as "regular Slack web-client" does), hence additional pip extension has to be installed:

`pip install websocket-client` (you may need root access)


#### notification_center.py:

> NOTE: notification_center.py plugin is macOS-only - for other notification systems - seek for compatible "notify" plugin here: https://weechat.org/scripts/). Additional pip extension has to be installed:

`pip install pync` (you may need root access)


## Installation:

* Copy `plugins/*.pl` files to: `~/.weechat/perl/autoload`

* Copy `plugins/*.py` files to: `~/.weechat/python/autoload`

* Copy `themes/*` files to: `~/.weechat/themes`. If you don't like `flashcode.theme` (my fav), you can find more themes here: https://weechat.org/themes/.

* Restart `weechat` :)


## wee_slack.py detailed usage and docs:

https://github.com/wee-slack/wee-slack
