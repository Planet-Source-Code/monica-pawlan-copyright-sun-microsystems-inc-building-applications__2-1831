<div align="center">

## Building Applications


</div>

### Description

All programs written in the JavaTM language (Java programs) are built from classes. Because all classes have the same structure and share common elements, all Java programs are very similar.

This lesson describes the structure and elements of a simple application created from one class. The next lesson (Buidling Applets) covers the same material for applets.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Monica Pawlan \(Copyright Sun Microsystems Inc\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/monica-pawlan-copyright-sun-microsystems-inc.md)
**Level**          |Beginner
**User Rating**    |4.8 (53 globes from 11 users)
**Compatibility**  |Java \(JDK 1\.1\)
**Category**       |[Complete Applications](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/complete-applications__2-64.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/monica-pawlan-copyright-sun-microsystems-inc-building-applications__2-1831/archive/master.zip)





### Source Code

<table border="0" cellPadding="0" cellSpacing="0">
 <tbody>
  <tr>
   <td>
    <table>
     <tr>
      <td width="*"><font face="verdana,Arial" size="3"><font face="verdana,arial"><center>
       <table bgColor="white" width="100%">
        <tbody>
         <tr>
          <td>
           <div align="center">
            <table border="0" width="100%">
             <tbody>
              <tr>
               <td width="100%"><font face="verdana,arial">
                <table border="0" cellPadding="0" cellSpacing="0">
                 <tbody>
                  <tr>
                   <td>
                    <table border="0" cellPadding="0" cellSpacing="0">
                     <tbody>
                      <tr>
                       <td vAlign="top">
                        <div align="right">
                         <div align="right">
                          <div align="right">
                           <h2 align="left"><font face="Verdana, Arial, Helvetica, sans-serif" size="5">Building
                           Applications</font></h2>
                           <p align="left"><font face="Verdana"><font size="3"><b>by
                           Monica Pawlan</b></font><br>
                           <b><font size="2">Reprinted
                           with permission from the <a href="http://developer.java.sun.com/developer/" target="_blank">Java
                           Developer Connection</a>(SM)<br>
                           </font></b></font><font size="2"><b><font face="verdana,arial">Copyright
                           <a href="http://www.sun.com" target="_blank">Sun
                           Microsystems Inc</a>.</font></b></p>
                           </font>
                           <hr>
                          </div>
                         </div>
                        </div>
                        <p><font face="Verdana">All
                        programs written in the Java<font size="-2"><sup>TM</sup></font>
                        language (Java programs) are
                        built from classes. Because all
                        classes have the same structure
                        and share common elements, all
                        Java programs are very similar.</font>
                        <p><font face="Verdana">This
                        lesson describes the structure
                        and elements of a simple
                        application created from one
                        class. The next lesson covers
                        the same material for applets.</font>
                        <ul>
                         <li><a href="#class"><font face="Verdana">Application
                          Structure and Elements</font></a>
                         <li><a href="#fields"><font face="Verdana">Fields
                          and Methods</font></a>
                         <li><a href="#const"><font face="Verdana">Constructors</font></a>
                         <li><a href="#more"><font face="Verdana">More
                          Information</font></a></li>
                        </ul>
                        <font face="Verdana, Arial, Helvetica, sans-serif">
                        <hr>
                        <a name="class"></a></font>
                        <h3><font face="Verdana">Application
                        Structure and Elements</font></h3>
                        <font face="Verdana"><img align="left" hspace="10" src="http://www.planet-source-code.com/vb/tutorial/java/images/class.gif">
                        An application is created from
                        classes. A <code>class</code> is
                        similar to a <code>RECORD</code>
                        in the Pascal language or a <code>struct</code>
                        in the C language in that it
                        stores related data in <i>fields</i>,
                        where the fields can be
                        different types. So you could,
                        for example, store a text string
                        in one field, an integer in
                        another field, and a floating
                        point in a third field. The
                        difference between a class and a
                        <code>RECORD</code> or <code>struct</code>
                        is that a class also defines the
                        <i>methods</i> to work on the
                        data.</font>
                        <p><font face="Verdana">For
                        example, a very simple class
                        might store a string of text and
                        define one method to set the
                        string and another method to get
                        the string and print it to the
                        console. Methods that work on
                        the data are called <i>accessor</i>
                        methods.</font>
                        <p><font face="Verdana"><img align="left" hspace="10" src="http://www.planet-source-code.com/vb/tutorial/java/images/main.gif">
                        Every application needs one
                        class with a <code>main</code>
                        method. This class is the entry
                        point for the program, and is
                        the class name passed to the <code>java</code>
                        interpreter command to run the
                        application.</font>
                        <p><font face="Verdana">The code
                        in the <code>main</code> method
                        executes first when the program
                        starts, and is the control point
                        from which the controller class
                        accessor methods are called to
                        work on the data.</font>
                        <p><font face="Verdana">Here,
                        again, is the <a href="http://www.planet-source-code.com/vb/tutorial/java/samples/ExampleProgram.java">example
                        program</a> from Lesson 1. It
                        has no fields or accessor
                        methods, but because it is the
                        only class in the program, it
                        has a <code>main</code> method.<br clear="all">
                        </font>
                        <pre><font face="Verdana">  class ExampleProgram {
   public static void main(String[] args){
    System.out.println(&quot;I'm a Simple Program&quot;);
   }
  }
</font></pre>
                        <p><font face="Verdana"><a name="instance"></a>The
                        <code>public static void</code>
                        keywords mean the Java<a href="#TJVM"><sup>1</sup></a>
                        virtual machine (JVM)
                        interpreter can call the
                        program's <code>main</code>
                        method to start the program
                        (public) without creating an
                        instance of the class (static),
                        and the program does not return
                        data to the Java VM interpreter
                        (void) when it ends.</font>
                        <p><font face="Verdana"><img align="left" hspace="10" src="http://www.planet-source-code.com/vb/tutorial/java/images/instance.gif">
                        An instance of a class is an
                        executable copy of the class
                        While the class describes the
                        data and behavior, you need a
                        class instance to acquire and
                        work on data. The diagram at the
                        left shows three instances of
                        the <code>ExampleProgram</code>
                        class by the names: <code>FirstInstance</code>,
                        <code>SecondInstance</code> and <code>ThirdInstance</code>.</font>
                        <p><font face="Verdana">The <code>main</code>
                        method is static to give the
                        Java VM interpreter a way to
                        start the class without creating
                        an instance of the control class
                        first. Instances of the control
                        class are created in the <code>main</code>
                        method after the program starts.</font>
                        <p><font face="Verdana">The <code>main</code>
                        method for the simple example
                        does not create an instance of
                        the <code>ExampleProgram</code>
                        class because none is needed.
                        The <code>ExampleProgram</code>
                        class has no other methods or
                        fields, so no class instance is
                        needed to access them from the <code>main</code>
                        method. The Java platform lets
                        you execute a class without
                        creating an instance of that
                        class as long as its static
                        methods do not call any
                        non-static methods or fields.</font>
                        <p><font face="Verdana">The <code>ExampleProgram</code>
                        class just calls <code>println</code>,
                        which is a static method in the <code>System</code>
                        class. The <code>java.lang.System</code>
                        class, among other things,
                        provides functionality to send
                        text to the terminal window
                        where the program was started.
                        It has all static fields and
                        methods.</font>
                        <p><font face="Verdana">The
                        static fields and methods of a
                        class can be called by another
                        program without creating an
                        instance of the class. So, just
                        as the Java VM interpreter
                        command could call the <code>static
                        main</code> method in the <code>ExampleProgram</code>
                        class without creating an
                        instance of the <code>ExampleProgram</code>
                        class, the <code>ExampleProgram</code>
                        class can call the <code>static
                        println</code> method in the <code>System</code>
                        class, without creating an
                        instance of the <code>System</code>
                        class.</font>
                        <p><font face="Verdana">However,
                        a program must create an
                        instance of a class to access
                        its non-static fields and
                        methods. Accessing static and
                        non-static fields and methods is
                        discussed further with several
                        examples in the next section. <a name="fields"></a></font>
                        <h3><font face="Verdana">Fields
                        and Methods</font></h3>
                        <font face="Verdana">The <a href="http://www.planet-source-code.com/vb/tutorial/java/samples/LessonTwoA.java">LessonTwoA.java</a>
                        program alters the simple
                        example to store the text string
                        in a static field called <code>text</code>.
                        The <code>text</code> field is
                        static so its data can be
                        accessed directly without
                        creating an <em>instance</em> of
                        the <code>LessonTwoA</code>
                        class.</font>
                        <pre><font face="Verdana">class LessonTwoA {
  static String text = &quot;I'm a Simple Program&quot;;
  public static void main(String[] args){
    System.out.println(text);
  }
}
</font></pre>
                        <font face="Verdana">The <a href="http://www.planet-source-code.com/vb/tutorial/java/samples/LessonTwoB.java">LessonTwoB.java</a>
                        and <a href="http://www.planet-source-code.com/vb/tutorial/java/samples/LessonTwoC.java">LessonTwoC.java</a>
                        programs add a <code>getText</code>
                        method to the program to
                        retrieve and print the text.</font>
                        <p><font face="Verdana">The <a href="http://www.planet-source-code.com/vb/tutorial/java/samples/LessonTwoB.java">LessonTwoB.java</a>
                        program accesses the non-static <code>text</code>
                        field with the non-static <code>getText</code>
                        method. Non-static methods and
                        fields are called instance
                        methods and fields. This
                        approach requires that an
                        instance of the <code>LessonTwoB</code>
                        class be created in the <code>main</code>
                        method. To keep things
                        interesting, this example
                        includes a static text field and
                        a non-static instance method (<code>getStaticText</code>)
                        to retrieve it.</font><font face="Verdana, Arial, Helvetica, sans-serif">
                        <blockquote>
                         <hr>
                        </font><font face="Verdana"><strong>Note:</strong>
                        The field and method return
                        values are all type <code>String</code>.</font><font face="Verdana, Arial, Helvetica, sans-serif">
                        <hr>
                        </blockquote>
                        </font>
                        <pre><font face="Verdana">class LessonTwoB {
  String text = &quot;I'm a Simple Program&quot;;
  static String text2 = &quot;I'm static text&quot;;
  String getText(){
    return text;
  }
  String getStaticText(){
    return text2;
  }
  public static void main(String[] args){
    LessonTwoB progInstance = new LessonTwoB();
    String retrievedText = progInstance.getText();
    String retrievedStaticText =
         progInstance.getStaticText();
    System.out.println(retrievedText);
    System.out.println(retrievedStaticText);
  }
}
</font></pre>
                        <font face="Verdana">The <a href="http://www.planet-source-code.com/vb/tutorial/java/samples/LessonTwoC.java">LessonTwoC.java</a>
                        program accesses the static <code>text</code>
                        field with the static <code>getText</code>
                        method. Static methods and
                        fields are called class methods
                        and fields. This approach allows
                        the program to call the static <code>getText</code>
                        method directly without creating
                        an instance of the <code>LessonTwoC</code>
                        class.</font>
                        <pre><font face="Verdana">class LessonTwoC {
  static String text = &quot;I'm a Simple Program&quot;;
//Accessor method
  static String getText(){
    return text;
  }
  public static void main(String[] args){
    String retrievedText = getText();
    System.out.println(retrievedText);
  }
}
</font></pre>
                        <font face="Verdana">So, class
                        methods can operate only on
                        class fields, and instance
                        methods can operate on class and
                        instance fields.</font>
                        <p><font face="Verdana">You
                        might wonder what the difference
                        means. In short, there is only
                        one copy of the data stored or
                        set in a class field but each
                        instance has its own copy of the
                        data stored or set in an
                        instance field.</font>
                        <p><font face="Verdana"><img src="http://www.planet-source-code.com/vb/tutorial/java/images/diff.gif"></font>
                        <p><font face="Verdana">The
                        figure above shows three class
                        instances with one static field
                        and one instance field. At
                        runtime, there is one copy of
                        the value for static Field A and
                        each instance points to the one
                        copy. When setFieldA(50) is
                        called on the first instance,
                        the value of the one copy
                        changes from 36 to 50 and all
                        three instances point to the new
                        value. But, when setFieldB(25)
                        is called on the first instance,
                        the value for Field B changes
                        from 0 to 25 for the first
                        instance only because each
                        instance has its own copy of
                        Field B.</font>
                        <p><font face="Verdana">See <a href="http://java.sun.com/docs/books/tutorial/java/javaOO/classvars.html" target="_blank">Understanding
                        Instance and Class Members</a>
                        lesson in <a href="http://java.sun.com/docs/books/tutorial/index.html" target="_blank">The
                        Java tutorial</a> for a thorough
                        discussion of this topic. <a name="const"></a></font>
                        <h3><font face="Verdana">Constructors</font></h3>
                        <font face="Verdana">Classes
                        have a special method called a <em>constructor</em>
                        that is called when a class
                        instance is created. The class
                        constructor always has the same
                        name as the class and no return
                        type. The <a href="http://www.planet-source-code.com/vb/tutorial/java/samples/LessonTwoD.java">LessonTwoD</a>
                        program converts the <code>LessonTwoB</code>
                        program to use a constructor to
                        initialize the text string.</font><font face="Verdana, Arial, Helvetica, sans-serif">
                        <blockquote>
                         <hr>
                        </font><font face="Verdana"><strong>Note:</strong>
                        If you do not write your own
                        constructor, the compiler adds
                        an empty constructor, which
                        calls the no-arguments
                        constructor of its parent class.
                        The empty constructor is called
                        the default constructor. The
                        default constructor initializes
                        all non-initialized fields and
                        variables to zero.</font><font face="Verdana, Arial, Helvetica, sans-serif">
                        <hr>
                        </blockquote>
                        </font>
                        <pre><font face="Verdana">class LessonTwoD {
  String text;
//Constructor
  LessonTwoD(){
   text = &quot;I'm a Simple Program&quot;;
  }
//Accessor method
  String getText(){
    return text;
  }
  public static void main(String[] args){
    LessonTwoD progInst = new LessonTwoD();
    String retrievedText = progInst.getText();
    System.out.println(retrievedText);
  }
}
</font></pre>
                        <font face="Verdana, Arial, Helvetica, sans-serif"><a name="summ"></a></font>
                        <h3><font face="Verdana">To
                        Summarize</font></h3>
                        <font face="Verdana">A simple
                        program that prints a short text
                        string to the console would
                        probably do everything in the <code>main</code>
                        method and do away with the
                        constructor, <code>text</code>
                        field, and <code>getText</code>
                        method. But, this lesson used a
                        very simple program to show you
                        the structure and elements in a
                        basic Java program. <a name="more"></a></font>
                        <h3><font face="Verdana">More
                        Information</font></h3>
                        <font face="Verdana">See <a href="http://java.sun.com/docs/books/tutorial/java/javaOO/classvars.html" target="_blank">Understanding
                        Instance and Class Members</a>
                        lesson in <a href="http://java.sun.com/docs/books/tutorial/index.html" target="_blank">The
                        Java tutorial</a> for a thorough
                        discussion of this topic.</font>
                        <p><font face="Verdana">_______<br>
                        <a name="TJVM"><sup>1</sup></a>
                        As used on this web site, the
                        terms &quot;Java virtual
                        machine&quot; or &quot;JVM&quot;
                        mean a virtual machine for the
                        Java platform.<br>
                        </font>
                        <hr>
                        <!--BEGIN READER SURVEY-->
                        <font size="2">
                        <p><font face="verdana,arial"><b>Reprinted
                        with permission from the <a href="http://developer.java.sun.com/developer/" target="_blank">Java
                        Developer Connection(SM)</a><br>
                        Copyright <a href="http://www.sun.com" target="_blank">Sun
                        Microsystems Inc</a>.</b></font></p>
                        </font>
                        <p align="right"><font face="Verdana" size="-1">[<a href="#top">TOP</a>]</font></p>
                       </td>
                      </tr>
                     </tbody>
                    </table>
                    <font face="Verdana, Arial, Helvetica, sans-serif"><!-- ================ -->
                    <!-- End Main Content -->
                    <!-- ================ -->
                    </font></td>
                  </tr>
                 </tbody>
                </table>
                <!-- Copyright Insert -->
                </font></td>
              </tr>
             </tbody>
            </table>
                     </td>
         </tr>
        </tbody>
       </table>
       </font><br>
       &nbsp;<br>
              &nbsp;</center></font></td>
     </tr>
    </table>
    <p>&nbsp;</td>
  </tr>
 </tbody>
</table>
<!-- Copyright Insert -->

