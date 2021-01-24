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

--build ......... scans your entire system and builds a catalog in $HOME/.mugplayer.json
--dups  ......... shows duplicate MP3 in your system
--play tag ...... plays a MP3 in the background by finding it using partial name / tag search
--stop .......... stops all music
--stats ......... shows stats that reveals which songs (MP3) you play the most, when, etc.

FUTURE TODO
1. Allow viewing play stats -- see what you play the most
2. Create/modify/delete playlists
3. Automatic playlist 'popular' which plays songs that you play the most

===============================================================================
WHY CREATE mugplayer?
If you are well organized and keep your music neatly organized and love
the Apple Music player, you don't need this tool.

I don't like playing music using the Apple's default music player.
And I am not organized when it comes to my MP3 music files. So I prefer
the system to find the music using part of the name or a tag and play
it in the background while I am working on a terminal.
===============================================================================
