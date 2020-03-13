# Closable Frame
A Frame doesnot have a close function in itslef. We have to write some codes to make the frame window close. We can close the AWT Window or Frame by calling dispose() or System.exit() inside windowClosing() method. The windowClosing() method is found in WindowListener interface and WindowAdapter class.

The WindowAdapter class implements WindowListener interfaces. It provides the default implementation of all the 7 methods of WindowListener interface. To override the windowClosing() method, you can either use WindowAdapter class or WindowListener interface.

If you implement the WindowListener interface, you will be forced to override all the 7 methods of WindowListener interface. So it is better to use WindowAdapter class.




# How do you handle events listner interface with its method with an example?

Java adapter classes provide the default implementation of listener interfaces. If you inherit the adapter class, you will not be forced to provide the implementation of all the methods of listener interfaces. So it saves code.

The adapter classes are found in java.awt.event, java.awt.dnd and javax.swing.event packages.

java.awt.event Adapter Classes

Adapter class	            Listener interface
WindowAdapter =>	        WindowListener
KeyAdapter	              KeyListener
MouseAdapter	            MouseListener
MouseMotionAdapter	      MouseMotionListener
FocusAdapter	            FocusListener
ContainerAdapter	        ContainerListener
HierarchyBoundsAdapter	  HierarchyBoundsListener
java.awt.dnd               Adapter classes

Adapter class	Listener interface
DragSourceAdapter	DragSourceListener
DragTargetAdapter	DragTargetListener
javax.swing.event Adapter classes

Adapter class	Listener interface
MouseInputAdapter	MouseInputListener
InternalFrameAdapter	InternalFrameListener
KeyAdapter Example;

MouseAdapter Example;

MouseMotionAdapter Example;



# Commonly used Event Listner

ActionListener

The Java ActionListener is notified whenever you click on the button or menu item.
It has 1 method:
public abstract void actionPerformed(ActionEvent e);
Example
MouseListener

The Java MouseListener is notified whenever you change the state of mouse.
It has 5 methods:
public abstract void mouseClicked(MouseEvent e);
public abstract void mouseEntered(MouseEvent e);
public abstract void mouseExited(MouseEvent e);
public abstract void mousePressed(MouseEvent e);
public abstract void mouseReleased(MouseEvent e);
Example
MouseMotionListener

The Java MouseMotionListener is notified whenever you move or drag mouse.
It has 2 methods:
public abstract void mouseDragged(MouseEvent e);
public abstract void mouseMoved(MouseEvent e);
Example
KeyListener

The Java KeyListener is notified whenever you change the state of key.
It has 3 methods:
public abstract void keyPressed(KeyEvent e);
public abstract void keyReleased(KeyEvent e);
public abstract void keyTyped(KeyEvent e);
Example
ItemListener

The Java ItemListener is notified whenever you click on the checkbox.
It has 1 method:
public abstract void itemStateChanged(ItemEvent e);
Example
WindowListener

The Java WindowListener is notified whenever you change the state of window.
It has 7 methods:
public abstract void windowActivated(WindowEvent e);
public abstract void windowClosing(WindowEvent e);
public abstract void windowClosed(WindowEvent e);
public abstract void windowDeactivated(WindowEvent e);
public abstract void windowDeiconified(WindowEvent e);
public abstract void windowIconified(WindowEvent e);
public abstract void windowOpened(WindowEvent e);


# How to handle events with an adaptar class?

Action Event Class
An Action Event is generated when:
a button is pressed.
a list item is double clicked.
menu item is clicked.
Constructor
ActionEvent(Object src, int type, String cmd)
ActionEvent(Object src, int type, String cmd, int modifiers)
ActionEvent(Object src, int type, String cmd, long when, int modifiers)
Here,
src = reference to the object that generated this event.
type = Determine type of event
cmd = command string
modifier = indicates modifier keys (ALT, CTRL, SHIFT); values are ALT_MASK, CTRL_MASK, SHIFT_MASK
when = specifies when the event occured

You can obtain the command name for the envoking ActionEvent object by using: String getActionCommand()
For eg:

When a button is pressed, an action event is generated that has a command name equal to the label on that button.

Other Methods :

int getModifier()
long getWhen()

KeyEvent Class
It is generated when:
Keyboard input occurs
Types of KeyEvent
KEY_PRESSED - generated when key is pressed.
KEY_RELEASED - generated when key is released.
KEY_TYPED - generated when key is generated.
Constants
VK_ALT, VK_DOWN, VK_LEFT, VK_RIGHT, VK_ENTER, VK_ESCAPE, VK_CONTROL, VK_SHIFT,

Methods
char getKeyChar ();
int getKeyChar ();
Mouse Event
There are eight types of mouse events:
Eight integer constants are defined to determine types:
MOUSE EVENT	Generate
MOUSE_CLICKED	When user clicked the mouse
MOUSE_DRESSED	The user dragged the mouse
MOUSE_ENTERED	The mouse entered a component
MOUSE_EXITED	The mouse exited from a component
MOUSE_MOVED	The mouse moved
MOUSE_PRESSED	The mouse was pressed
MOUSE_RELEASED	The mouse was released
MOUSE_WHEEL	The mouse wheel was moved.
Methods:
int getX()
int getY()
Point getPoint() -> gives object that contain X, Y co-ordinates
int getClickCount()
boolean isPopupTrigger() -> tests if this events causes a pop-up menu to appear on this platform.
int getButton() -> returns a values that represents the button that caused the event.
