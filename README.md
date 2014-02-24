winterface
==========

A super-basic Windows-only Python mouse-and-keyboard simulator. Status: somewhat but not entirely unlike stable.

# Examples of Use Cases
- ## iTunes Manipulation
 The other day, I bought a higher-bitrate version of a few songs I've played a million times in iTunes. There's no way to manually adjust the play-count of a track in iTunes, but I often sort these songs by 'Play.' So I had to play my new audio files hundreds of times to make them match their older counterparts before deleting the old ones.

 First, I turned on 'repeat-one' to replay a song after it ended. Then I used `getMousePos()` to find the pixel location of the song's ending in the trackbar, which (when you click it) ends the song and starts it over as though it's been played in full.

 Finally, I used this script to match play-counts:
     
         import winterface
         def replay(n): 
             for i in range(n):
                 abortCheck(0.25);
                 click(994,42)
            
 *Et voila!*
 
- ## Drawing Straight Lines in Paint
 ...not sure how frequently you have to do this, but `drag(10, 10, 10, 20)` will draw a 10px straight line.

- ## Spam-Clicking Until User Moves Mouse
 Simply run this loop:

        import winterface
        abortCheck() # make sure you haven't moved the mouse
        click(0, 0)  # click.


# More Details

I wrote a huge readme in an online markdown editor and then my internet died and I lost it all. So here. This.


    def pixelAt(x, y):
        """Return a pixel color at (x, y) --> Hex"""
    
    def abortCheck(delay = 3):
        """Wait <delay> seconds, and quit on mouse move."""
    
    def moveOnPixelChange(x, y, delay = 0):
        """Return from function when the pixel changes color [after <delay> seconds]"""
    
    def drag(x0, y0, x1, y1, delay=0):
        """Click and drag x0 y0 to x1 y1"""
            
    
    def click(x, y, click=True, left=True):
        """Click at (x, y) (default left click)"""
    
    def mouse(x1, y1, click1=False, left=True, speed='fast')
        """Move the mouse to x1, y1."""
    
    
    def dokey(key1,key2=None):
        """Simulate the typing of ascii key1"""
    
    def doSkey(key1,key2=None):
        """Simulate the typing of char key1"""
    
    def ctrlAlt(key3):
        """Press CTRL+ALT+key3"""
    
    def ca(s):
        """Return the integer version of some char s (useful for dokey())"""
    
    def type_string(s):
        """Type a string s"""
    
    def getMousePos(delay = 0):
        """Get the mouse (x, y) after <delay> seconds"""
    
    def clipTextAt(x0, y0, x1, y1):
        """Copies the text to the clipboard (and returns it)"""



You also get these: 
    `SCREEN_WIDTH`, `SCREEN_HEIGHT`, `ENTER`, `TAB`, `SHIFT`, `CTRL`, `ALT`, `BACKSPACE`, `LEFT`, `UP`, `RIGHT`, `DOWN`,     `WIN`, `F6`, `F11`, `NUM1`, `NUM2`, `NUM3`, `NUM4`

