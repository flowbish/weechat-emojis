The shittiest weechat plugin ever. Automagical emojis!
------------------------------------------------------------------------------

                    :sparkles::boom::star: INSTRUCTIONS :+1::sparkles::star2:

1. Copy/symlink script as `~/.weechat/python/emojis.py`
2. Copy/symlink emojis database as `~/.weechat/emojis-db.dat`
3. `/script load emojis.py`
4. Marvel at your ability to use things like :horse:

Optional:

Symlink into `~/.weechat/python/autoload` to load automatically

You can configure an arbitrary path for the emojis database:
    /set plugins.var.python.emojis.dbfile /path/to/emojis-db.dat

You can reload the emojis using
    /emoji reload
  
You can add an emoji from within weechat using
    /emoji add <name> <emoji>
  
To display a particular emoji (without sending it to a buffer) use
    /emoji show <name>
  
`emojis.py` supports tab-completion as well!

You may add your own to the database, format is:

    :trigger:
    emoji

Your trigger MUST be surrounded with ':'.

The format is compatible with irssi-emojis and the mirc variant from
Daniel Callander (Knifa).

NOTE: The script currently doesn't work over weechat relay clients. This is
because it hooks the input buffer event explicitly, and as such will only work
in the curses client.

                   (ノ゜o゜)ノ　　　　●～*　　　　　Σ(゜д゜)
     ATTENTION: This is a preliminary port of the irssi analogue found at:
                    https://github.com/mrdaemon/irssi-emojis
  It may not be as featureful at the moment, but the basics work, and sanely.
