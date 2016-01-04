The shittiest weechat plugin ever. Automagical emojis!
------------------------------------------------------------------------------

##:sparkles::boom::star: Installing :+1::sparkles::star2:

1. Copy/symlink script as `~/.weechat/python/emojis.py`
2. Copy/symlink emojis database as `~/.weechat/emojis-db.dat`
3. Run `/script load emojis.py` in weechat
4. Marvel at your ability to use things like `:horse:`

Optional:

Symlink into `~/.weechat/python/autoload` to load automatically. :ok_hand:

You can configure an arbitrary path for the emojis database:

    /set plugins.var.python.emojis.dbfile /path/to/emojis-db.dat

## Using emojis.py! :joy::cat2:

Instances of an emoji's common name (`:horse:`) get translated into its beautiful, pictographic form! :horse: Its as easy as that!

It may also be a good idea to comb through the database and modify the names of your most commonly-used emoji, as `:reversed_hand_with_middle_finger_extended:` is a bit of a mouthfull.

You can reload emojis from the database file using

    /emoji reload
  
You can add an emoji from within weechat with

    /emoji add <name> <emoji>
  
To display a particular emoji (without sending it to a buffer) use

    /emoji show <name>
  
`emojis.py` supports tab-completion as well! :fire::fire::pray:

## Adding your own 'mojis :ok_hand::+1:

You may add your own to the database, format is:

    :trigger:
    emoji

Your trigger MUST be surrounded with `:`.

The format is compatible with irssi-emojis and the mirc variant from
Daniel Callander (Knifa).

NOTE: The script currently doesn't work over weechat relay clients. This is
because it hooks the input buffer event explicitly, and as such will only work
in the curses client.

                   (ノ゜o゜)ノ　　　　●～*　　　　　Σ(゜д゜)
     ATTENTION: This is a preliminary port of the irssi analogue found at:
                    https://github.com/mrdaemon/irssi-emojis
  It may not be as featureful at the moment, but the basics work, and sanely.
