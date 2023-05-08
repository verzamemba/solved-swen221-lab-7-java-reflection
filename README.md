Download Link: https://assignmentchef.com/product/solved-swen221-lab-7-java-reflection
<br>
The purpose of this Lab is to give you hands on practice using Java reflection.

<h2>1        A Widget System</h2>

The program provided with this lab implements a very primitive <em>widget system </em>which is inspired by modern windowing systems. In this system <em>widgets </em>occupy areas on the screen and can respond to mouse clicks. Widgets have internal state which they can use to control how they look. The following illustrates a simple widget system:

Here we see a very simple widget systems constructed from <em>five </em>widgets. The four visible squares each constitute one widget, whilst the <em>background </em>itself constitutes another widget. The two widgets on the top row are <em>toggles </em>— when clicked on, they will change to either the <em>on </em>or <em>o↵ </em>state. The two widgets on the bottom row are <em>counters </em>— when clicked on, they will increment an internal counter and set their counter according to this.

<h2>2       What to do</h2>

The key challenge in this lab lies in interacting with widgets through reflection. In particular, <em>you will be unable to see the source code for one of the widgets</em>. This means that reflection provides the only way in which you can interact with this widget. The <em>Inspector </em>provides the skeleton for a suite of methods for creating widgets and reading/writing their attributes. Some notes:

<ul>

 <li>newWidget(String name, Rectangle dimensions). This instantiates a new instance of the class given by name. To do this, you will need to first find the appropriate constructor in the widget’s class, and then instantiate a new object using Constructor.newInstance().</li>

 <li>getAttribute(Widget widget, String name). This reads the value of field name in the given widget. To do this, it must call the corresponding “getter” method. For example, for a field called color the corresponding getter would be getColor().</li>

 <li>setAttribute(Widget widget, String name, Object value). This writes a given value into field name in the given widget. To do this, it must call the corresponding “setter” method. For example, for a field named color of type Color the corresponding setter would be setColor(Color).</li>

</ul>

<em>Your goal in this lab is to complete the above methods in the Inspector class.</em>