winterface
==========

A super-basic Windows-only Python mouse-and-keyboard simulator. Status: somewhat but not entirely unlike stable.


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
    SCREEN_WIDTH, SCREEN_HEIGHT, ENTER, TAB, SHIFT, CTRL, ALT, BACKSPACE, LEFT, UP, RIGHT, DOWN, WIN, F6, F11, NUM1, NUM2, NUM3, NUM4

