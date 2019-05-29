# Hello-World
My first repository.

Hi. I'm pretty new to coding. All I know is HTML and CSS. What I would like to do is create a language called DSS (for Dynamic Style Sheets.) This language would work directly with other stylesheet languages (CSS, SASS, SCSS, LESS), and also with HTML. 
Two of the main features of DSS would be the allowance of multiple actions on a single event, and the reduction of code writing by a feature called "cabwa", which stands for "Can Also Be Written As". The cabwa feature can be used for DSS itself, and also for CSS. 
Example: Make it easier to create 3D boxes. First, write out the long-hand for creating a cube in CSS, like this:
code?is "(The code for making a cube. The actual code though, not that statement.)" {
  cabwa
  box-width: 'num';
  box-height: 'num';
  box-depth: 'num'; 
  
  Example: #header-box {
    box-width: 1000px;
    box-height: 200px;
    box-depth: 300px;
    (As well as other modifiers like background-color/image/gradient for each face, any borders, etc)
    }
    
A global cabwa file can be created (although the extention would be .dss) as an external file, so that those pre-defined shorthand codes can be used through the entire site ( lie a stylesheet or script file.) Otherwise, the cabwa defs can be written in the &lt; style &gt; tag within the &lt; head &gt; tag of the document, and be used only for that particular document.   

Example of allowing multiple events:

event?is on-click?for e-id?is 'link', action?is {
  display? message('Directing you to the next page.');
  open? 'next-page.html';
  }
(Which says, "There is an event, which is the on-click event, which is for this id, which is 'link'. The action for this event is..." Which cabwa:)
 
 event? on-click? e-id?is 'link', action?is display? message('Directing you to the next page.') then open? 'next-page.html';
 
 The "then" statement determines the order in which actions are done, so they aren't done at the same time or in the wrong order. 
 (Also, "e-id" stands for "element id", as opposed to "s-id" for "style id". The program would work with just "id", but the e or s helps it to know ahead of time what it's looking for so it can run more quickly.)
 
 One other feature will be mentioned here, although this will not by any means be the entirety of the description of DSS. The "make" statement, which is an action keyword. It alters the default property value of a gien element. 
  Example:
   event? on-hover? e-id?is 'main-content', action?is make overflow? visible;
   (whereas, the default property value of "overflow" [by styling] had been "hidden".)
