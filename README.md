## Requirements:

* Modern terminal with full UTF-8 support (iTerm, Terminal.app, Konsole, Gnome-terminal, urxvt, …).
* Weechat 2.2 (prebuilt version for macOS 10.11+ [is available here](http://software.verknowsys.com/binary/Darwin-10.11-x86_64/Weechat-2.2-Darwin-10.11-x86_64.txz)).
* Python 2.x (already installed under macOS).
* Perl 5.x (already installed under macOS).


### Additional dependencies:

* wee_slack.py:

`pip install websocket-client`


* notification_center.py:

`pip install pync`


## Installation:

* Copy `plugins/*.pl` files to: `~/.weechat/perl/autoload`

* Copy `plugins/*.py` files to: `~/.weechat/python/autoload`

* Copy `themes/*` files to: `~/.weechat/themes`. If you don't like `flashcode.theme` (my fav), you can find more themes here: https://weechat.org/themes/.

* Restart `weechat` :)


## wee_slack.py detailed usage and docs:

https://github.com/wee-slack/wee-slack
