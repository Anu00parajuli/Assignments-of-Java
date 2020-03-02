## Java Border Layouts(Border Managers)
The LayoutManagers are used to arrange components in a particular manner. LayoutManager is an interface that is implemented by all the classes of layout managers. 
There are following classes that represents the layout managers:

1.java.awt.BorderLayout <br/>
2.java.awt.FlowLayout <br/>
3.java.awt.GridLayout <br/>
4.java.awt.CardLayout <br/>
5.java.awt.GridBagLayout <br/>
6.javax.swing.BoxLayout <br/>
7.javax.swing.GroupLayout <br/>
8.javax.swing.ScrollPaneLayout <br/>
9.javax.swing.SpringLayout etc.<br/>

Out of the above mentioned border layouts, we are discussing only about three of them . And they are as follows:
1. Java Card Layout <br/>
2. Java Grid Layout <br/>
3. Java Flow Layout<br/>


# Java GridLayout
The GridLayout is used to arrange the components in rectangular grid. One component is displayed in each rectangle.

Constructors of GridLayout class  <br/>
1.GridLayout(): creates a grid layout with one column per component in a row. <br/>
2.GridLayout(int rows, int columns): creates a grid layout with the given rows and columns but no gaps between the components.<br/>
3.GridLayout(int rows, int columns, int hgap, int vgap): creates a grid layout with the given rows and columns alongwith given horizontal and vertical gaps.<br/>


# Java FlowLayout
The FlowLayout is used to arrange the components in a line, one after another (in a flow). It is the default layout of applet or panel.<br/>

Fields of FlowLayout class <br/>
1.public static final int LEFT <br/>
2.public static final int RIGHT<br/>
3.public static final int CENTER <br/>
4.public static final int LEADING <br/>
5.public static final int TRAILING<br/>

Constructors of FlowLayout class <br/>
1.FlowLayout(): creates a flow layout with centered alignment and a default 5 unit horizontal and vertical gap.<br/>
2.FlowLayout(int align): creates a flow layout with the given alignment and a default 5 unit horizontal and vertical gap. <br/>
3.FlowLayout(int align, int hgap, int vgap): creates a flow layout with the given alignment and the given horizontal and vertical gap. <br/>



# Java CardLayout
The CardLayout class manages the components in such a manner that only one component is visible at a time. It treats each component as a card that is why it is known as CardLayout. <br/>

Constructors of CardLayout class <br/>
1.CardLayout(): creates a card layout with zero horizontal and vertical gap. <br/>
2.CardLayout(int hgap, int vgap): creates a card layout with the given horizontal and vertical gap.<br/>

Commonly used methods of CardLayout class <br/>
- public void next(Container parent): is used to flip to the next card of the given container. <br/>
- public void previous(Container parent): is used to flip to the previous card of the given container. <br/>
- public void first(Container parent): is used to flip to the first card of the given container. <br/>
- public void last(Container parent): is used to flip to the last card of the given container. <br/>
- public void show(Container parent, String name): is used to flip to the specified card with the given name. <br/>
