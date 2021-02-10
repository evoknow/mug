# Frequently Asked Questions and Answers

## Q: WHY CREATE mugplayer?
Answer: If you are well organized and keep your music neatly organized and love
the Apple Music player, you don't need this tool.

I don't like playing music using the Apple's default music player.
And I am not organized when it comes to my MP3 music files. So I prefer
the system to find the music using part of the title and play
it in the background while I am working on a terminal.



## Q: How to add item to the current queue?

Use --next title to add a song to the queue. Example:

$ mugplayer --next believe 

This adds the song with title or tag 'believe' to the queue and plays next. 

## Q: How do you play the current queue?

Use --play queue to play the songs in current queue. Example:

$ mugplayer --play queue

This will start playing the queue from where it left off or start from the top.

## Q: How to see what songs are queued?

Use --queue  to view the current queue. Example:

$ mugplayer --queue
1. Believe
2. Beat It
3. Dessert Rose

Shows an example queue of three songs.



