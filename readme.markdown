BEAM simple word cloud generator...

This software includes https://github.com/jdf/cue.language
and is licensed same as it is under Apache 2 license.

Usage:
// simple
String str = ""; // the string to create the cloud from - nb. read into memory!
int ng = 2;      // the n in n-gram - ie. how many words constitute a token

Cloud c1 = new Cloud();
c1.absorb(str, 2);
  
System.out.println(c1.toHTML());
  
// outputs (all return "String")
c1.toHTML();   // get output with font sizes in pixels
c1.toHTMLpc(); // get output with font sizes in %
c1.toHTMLem(); // get output with font sizes in ems

// options
c1.setMinFontSize(); // set minimum font size
c1.setMaxFontSize(); // you guessed it!
c1.setUSELOGCURVE(); // logorithmic rather than linear smoothing
c1.setScale();       // scales output for % & ems - try it and see what happens! :-)