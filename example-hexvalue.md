# Example (Hex Value)

An example of a regex expression of a hex value: /^#? ([a-f0-9]{6}|[a-f0-9]{3})$/ <br/>


Hex values of various colors: <br/>
    -red: #ff0000 <br/>
    -green: #00ff00 <br/>
    -blue: #0000ff <br/>


Regardless of the color and/or shade, all hex values have these traits in common: <br/> 

They all begin with '#', followed by six characters, which vary from any and all alphanumeric chars (lowercase a-z and digits 0-9). Now that the hex value rule has been established, the following will dissect the general regular expression of a hex value. <br/>

-**/' '/**: everything in the forward slash is considered in the expression <br/>
-**^#?**: matches '#' exactly 0-1 time; <br/>
          indicates that all hex values begin with '#'
-**([a-f0-9]{6}|[a-f0-9]{3})**: the 6-char string must contain a-f or 0-9 OR, <br/>
                                a 3-char string must contain a-f or 0-9 <br/>;
                                measures full hex value string, or a light value (2 chars, such as XXoooo, ooXXoo, or ooooXX, but 3 increases range of string)<br/>
-**$**: string ends, concluding the regex expression of the hex value

















