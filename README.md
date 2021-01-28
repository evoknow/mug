# MUG
Wecome to macOS User Group (MUG) Scripts and Files
Visit our YouTube Channel: https://macuser.group
====================================================================
We create experimental command-line tools for macOS.
USE THEM AS-IS AT YOUR OWN RISK! 
====================================================================

mugplayer -- a command-line mp3 player that scans your entire storage
for MP3 files and catalogs them into a JSON database in $HOME/.mugplayer.json

You can use this player to play a MP3 file using simple keyword which 
can be part of the name. Or you can add tags to each MP3 and access them
via tags.

You can also view duplicate MP3s in your system using --dups option.

Syntax: ./mugplayer --<option> [value]

Current command-line <option>s:

--build ................... scans your entire system and builds a catalog in $HOME/.mugplayer.json
--dups  ................... shows duplicate MP3 in your system
--play tag | playlist ...... plays a MP3 by tag or playlist name
--loop tag | playlist ...... plays a MP3 or playlist forever until stopped using --stop
--stop ..................... stops all music
--stats .................... shows stats that reveals which songs (MP3) you play the most, when, etc.

TODO LIST:
1. Play a song or playlist at a specific time --at hh:mm:ss (creates an AT job)
2. Building database using --build should retain old meta data
3. Create/modify/delete playlists

AUTOMATIC PLAYLIST:
* top{n} -- plays your top {n} songs based on stats

===============================================================================
WHY CREATE mugplayer?
If you are well organized and keep your music neatly organized and love
the Apple Music player, you don't need this tool.

I don't like playing music using the Apple's default music player.
And I am not organized when it comes to my MP3 music files. So I prefer
the system to find the music using part of the name or a tag and play
it in the background while I am working on a terminal.
===============================================================================
