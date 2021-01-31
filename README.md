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
* --stats ....................... shows stats that reveals which songs (MP3) you play the most, when, etc.
* --tag title | playlist <tag> .. tag the named title or playlist
* --dups ........................ shows duplicate songs in your system. 
* --dups remove.................. creates remove-dups.sh script that you can run to delete dups (BE CAREFUL! USE AT OWN RISK!)

## TODO ##
1. Play a song or playlist at a specific time --at hh:mm:ss (creates an AT job)
1. The --build should not lose existing meta data and stats 
1. Playlist support: create/modify/delete playlists
1. Tag support: create/modify/delete tags for songs and playlist
1. Add --copy playlist /path to allow copying the playlist to a /path (e.g. USB device)
1. If a song/tag exists, do not allow same title/tag to be used for creating a new playlist (BUG)

## AUTOMATIC PLAYLIST:
* top{n} -- plays your top {n} songs based on stats

## INSTALLATION ##
From the terminal prompt, do the following:
1. Fetch the source code from github using: git clone git@github.com:evoknow/mug.git
1. Change directory to the mug folder using the following command: `cd mug`
1. Run: `echo "alias mugplayer=$PWD/mugplayer" >> ~/.zshrc` to create a ZSH alias for easy access next time
1. Run: `source ~/.zshrc`

If you do not use `zsh` and use a different shell like `bash` then replace `.zshrc` with `.bashrc` in the above steps.


## Frequently Asked Questions and Answers ##
See FAQ.md