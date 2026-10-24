# HOW TO THE VibePONG game buildings

vibepong accepts .sheet files
a .sheet is constructed like this:

# 1. Preparation
  1. Get the audio you want to chart.
  2. Get the audio's BPM and offset with a program such as ArrowVortex.
  3. In a program such as audacity, trim the start to the offset ArrowVortex provides, then export it as WAV.
  4. Open any text editor, preferable the IDE under /vibepong/ide.html
  5. Insert the exported audio in the html file under Load Audio. Do not delete the file.
  6. Upon the first lines of the files, insert the following, and replace anything within square brackets in this example to what it requires:
    ```
    @bpm [bpm that arrowvortex provided]
    @src [exact audio file name without extension]
    @title [song name]
    @artist [who made the song]
    @diff [difficulty of the chart]
    ```
  7. Append `s` after the snippet above in a newline.
  8. Append `e` after the line of the inserted `s` line.
# 2. Charting
  Each chart is played from s (start) to e (end), and everything stops at the end.
  
  All actions must be placed in between the s and e lines.
  
  ## Actions List
   - `x[speed]` Multiply the speed of the game. IT IS BEST NOT TO SET `speed` TO ANYTHING EXCEPT ANY POWER OF TWO, NOT DOING SO MAY CAUSE THE GAME TO BREAK.
   - `w` Spawns a wall for the current beat. Offbeat, it will bounce the ball back to who it bounced from.
   - `m` Forces a miss in the current beat, also known as the gun mechanic
   - `v` The ball swerves on its own in the current beat back to who it bounced from. A miss is not forced.

   Multiple actions may be played in one beat by separating with `;`.

wip thing   
