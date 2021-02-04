# MUG #
Wecome to macOS User Group (MUG) Scripts and Files
Visit our YouTube Channel: https://macuser.group

We create experimental command-line tools for macOS.
USE THEM AS-IS AT YOUR OWN RISK! 

mugplayer -- a command-line mp3 player that scans your entire storage
for MP3 files and catalogs them into a JSON database in $HOME/.mugplayer.json

You can use this player to play a song using simple keyword which 
can be part of the name. Or you can add tags to each MP3 and access them
via tags.

You can also view duplicate MP3s in your system using --dups option.

Syntax: `mugplayer --<optoin> [value]`

## Available options: ##
* --build ....................... scans your entire system and builds a catalog in $HOME/.mugplayer.json
* --play title | tag | playlist . plays a song by title or tag or playlist name
* --loop title | tag | playlist . loops a song by title or tag or playlist until --stop is used to stop them
* --stop ........................ stops playing song or playlist
* --create <name> ............... creates a new playlist <name>
* --add title | tag <playlist>... adds the song by title or tag in the <playlist>
* --at "hh:mm:ss" title.......... play song by title at hh:mm:ss
* --stats ....................... shows stats that reveals which songs (MP3) you play the most, when, etc.
* --dups ........................ shows duplicate songs in your system. 

## Planned options: ##
* --delete <playlist> .............. deletes named playlist
* --delete <playlist> title | tag .. deletes the named song from the playlist by title or tag
* --tag title | playlist <tag> ..... tag the named title or playlist
* --xtag title | playlist <tag>..... removes the named tag from song or playlist
* --dups remove..................... creates remove-dups.sh script that you can run to delete dups (BE CAREFUL! USE AT OWN RISK!)
* --next tag | title ............... queues the song to play next
* --purge tag | title .............. removes a song by title or tag from database (not the actual mp3 file)
* --rmfile tag | title ............. deletes actual MP3 files matching the tag or title


## TODO ##
1. Playlist support: --delete <playlist> <tag> .. delete a song from the playlist or entire playlist
1. If a song/tag exists, do not allow same title/tag to be used for creating a new playlist (BUG)
1. Add --at "hh:mm:ss" playlist support
1. Tag support: create/delete tags for songs and playlist
1. The --build should not lose existing meta data and stats 
1. Add --copy playlist /path to allow copying the playlist to a /path (e.g. USB device)

## AUTOMATIC PLAYLIST:
* top{n} -- plays your top {n} songs based on stats
* never{n} -- plays {n} songs that you have never played using mugplayer
* lastplayed -- plays songs that you played {n}d {n}m {n}y ago


## INSTALLATION ##
From the terminal prompt, do the following:
1. Fetch the source code from github using: git clone git@github.com:evoknow/mug.git
1. Change directory to the mug folder using the following command: `cd mug`
1. Run: `echo "alias mugplayer=$PWD/mugplayer" >> ~/.zshrc` to create a ZSH alias for easy access next time
1. Run: `source ~/.zshrc`

If you do not use `zsh` and use a different shell like `bash` then replace `.zshrc` with `.bashrc` in the above steps.

## Frequently Asked Questions and Answers ##
See FAQ.md
