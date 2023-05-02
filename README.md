Download Link: https://assignmentchef.com/product/solved-cop3252-project-5
<br>
This assignment should give you practice with some aspects of working with graphics and windows in Java.

<h1>Task</h1>

Write a program utilizing a JDesktopFrame and menus to allow the user to create windows containing various graphics. You will have multiple files to turn in. <strong>At minimum</strong>, you will have the following files:

<ul>

 <li>java</li>

 <li>java</li>

</ul>

You may build other classes in other files. It is recommended that you create a class for each type of window being created, but this is not required. You may have as many classes as you want, as long as you reach the minimum (a lot of these classes could be represented as either stand-alone classes or inner classes, it is up to you where to draw the line). Everything will be packed up into a runnable jar file at the end.

<strong>Each file should have a comment including your name at the top of the file. Each file should also have appropriate comments throughout.</strong>

You will need to use the HW5Main.java file found <a href="http://ww2.cs.fsu.edu/~thrasher/cop3252/asg/HW5Main.java">here</a><a href="http://ww2.cs.fsu.edu/~thrasher/cop3252/asg/HW5Main.java">.</a>

<h1>Requirements</h1>

<ol>

 <li><strong>Storage and setup: </strong>You can design this with as many or as few classes as you like. The program must begin with the main() method in class HW5Main (which should not be changed), which will need access to a DesktopFrame class that extends JFrame.</li>

 <li><strong>DesktopFrame: </strong>Your DesktopFrame class should extend JFrame and have the following features:

  <ul>

   <li>Should contain a JDesktopPane on which to put the windows that will open</li>

   <li>Should contain a menu bar that contains two menus</li>

   <li>The first menu, “Create”, which will contain a listing for the windows that may be created</li>

   <li>This menu should be accessible by the mnemonic ’c’</li>

   <li>The second menu, “Quit”, will contain a single item ”Exit Program” that will close the program</li>

   <li>The Quit menu should have the mnemonic ’q’ and the ”Exit Program” menu item should have the mnemonic ’x’</li>

   <li>You will receive +1 extra credit for also implementing an accelerator for exiting the program (Ctrl + X)</li>

  </ul></li>

 <li><strong>Internal Windows</strong>: Upon selecting a menu item under the “Create” menu, a new JInternalFrame should be created, based on the selected item. Either a ”Picture Frame” or a ”Changeable Picture Frame” as discussed below.</li>

 <li><strong>Picture Frame</strong>: The first menu item under “Create” should have the text ”Picture Frame” and create a new JInternalFrame containing a picture created using Graphics, following the specification below:

  <ul>

   <li>The title of this frame should be ”Picture Frame”</li>

   <li>This menu option should be accessible by the mnemonic ’p’</li>

   <li>This frame should have a blue background.</li>

   <li>On this background, you should draw a circle and a rectangle.</li>

   <li>The circle should be yellow, have a width and height of 25% of the frame’s width or height (whichever is smaller at the time of painting), and be placed at a height about 10% from the top of the frame and about 30% from the right of the frame.</li>

   <li>The rectangle should cover the entire width of the frame and 10% of the height of the frame. It should be placed at the bottom of the frame and be colored brown.</li>

   <li>See the example screenshots for a better idea of what this picture should look like.</li>

  </ul></li>

 <li><strong>Changeable Picture Frame</strong>: The second menu item under “Create” should have the text ”Changeable Picture Frame” and create a new JInternalFrame containing a few items: a checkbox, 3 radio buttons, and a picture created using Graphics, following the specification below:

  <ul>

   <li>The frame’s title should be ”Changeable Picture Frame”</li>

   <li>This menu option should be accessible by the mnemonic ’c’</li>

   <li>The checkbox and radio buttons items should be above the picture and on the default background color.</li>

   <li>The checkbox should be labeled ”Move on Drag”</li>

   <li>The radio buttons should be labeled ”Green”, ”Red”, and ”Blue” and should all be in the same button group.</li>

   <li>The ”Green” radio button should be selected by default.</li>

   <li>The four UI objects should be evenly spaced across this panel.</li>

   <li>The picture itself should be in its own panel (below the UI), with a white background.</li>

   <li>On this background, you should draw a single oval.</li>

   <li>The oval’s color is determined by the UI object (so by default, it will be green)</li>

   <li>The oval should have a width and height of 30% of the panel’s width and height, respectively (so if the panel has a width of 100 and a height of 50, the oval should have a width of 30 and a height of 15), and should, by default, be placed in the center of the panel.</li>

   <li>If the checkbox is not checked, the circle should be placed in the center of the panel.</li>

   <li>If the checkbox is checked, the circle should remain where it is unless the user is actively clicking &amp; dragging the mouse on the panel. In that case, the circle should be <strong>centered </strong>on the mouse position. After releasing the mouse, the circle should remain where it is until either the checkbox becomes unchecked or the mouse is dragged again.</li>

   <li>See the example screenshots for a better idea of what this picture should look like.</li>

  </ul></li>

 <li><strong>Other Requirements/Hints:</strong>

  <ul>

   <li>For the first frame, be aware that there is no brown color constant, so you will have to use your best judgment to specify RGB values for brown. You do NOT have to match the brown in the screen shots exactly, but you will be counted off if you have a significantly different color (the rectangle shouldn’t be green, for example).</li>

   <li>Remember that you cannot draw directly on a JInternalFrame and must include another component in the frame to draw on, such as a JPanel</li>

   <li>Remember that internal frames are created with their visible property set to false and size set to 0, so you must set these if you want them to show up.</li>

   <li>When I discuss a percentage of a frame/panel’s height/width, I mean the current height/width, so if the frame is resized, the picture should change to fit the new size.</li>

   <li>All internal frames should be resizable, closable, maximizable, and iconifiable, as well as have a title (as indicated in the pictures).</li>

   <li>If something is not specified and not shown in the pictures, use your best judgment.</li>

   <li>You should be able to spawn multiple copies of each window and each should be independent of all the others.</li>

  </ul></li>

 <li><strong>Extra Credit (10%)</strong>: For extra credit, you may implement a third frame, listed in the menu as a ”Randomized Picture” which should follow these specifications:

  <ul>

   <li>This frame should have the title ”Randomized Picture”</li>

   <li>This menu option should be accessible by the mnemonic ’r’</li>

   <li>This picture should contain a random number of rectangles (1 to 5) drawn randomly on the screen.</li>

   <li>They should each be of a random color.</li>

   <li>They should be positioned at some random point in the frame (the rectangle’s location parameters should be within the frame, it is okay if some drawing takes place outside the frame).</li>

   <li>They should be of a random size, with width and height being randomly set independently between 1 pixel and of the frame width and frame height, respectively. Note that this means some rectangles will only partially be in the frame, this is okay.</li>

   <li>These rectangles should reset to new positions and colors (as well as a different number of rectangles) every time the frame is painted.</li>

   <li>If you implement this, spend a little time resizing/moving the frame around, it is a good way to see when the paintComponent method gets called.</li>

   <li>Be aware there may be some graphical artifacts that turn up sometimes if you drag one of these windows on top of the other, this is acceptable for the extra credit.</li>

  </ul></li>

</ol>

<h1>Sample Output</h1>

These pictures have implemented the extra credit option

The application with the Picture Frame created and the Create menu open.

The application with 2 Changeable Picture Frames open. The one on the left has been moved, the one on the right has not. This picture also shows the Quit menu open.

The application with 3 Randomized Picture Frames (the extra credit) open.