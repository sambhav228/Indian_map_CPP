# Indian_map_CPP

### Code to generate the map of India

Basically, the string is a run-length encoding of the map of India. Alternating characters in the string stores how many times to draw
a space, and how many times to draw an exclamation mark consecutively.

##### Totally two loop running here:
###### Outer for loop
        This loop goes over the characters in the string. Each iteration increases the value of b by one, and assigns the next character 
        in the string to a.
        
###### Inner for loop
      This loop draws individual characters, and a newline whenever it reaches the end of line. Consider this putchar statement
      putchar(++c=='Z' ? c = c/9 : 33^b&1);
      
As ‘Z’ represents number 90 in ASCII, 90/9 will give us 10 which is a newline character. Decimal 33 is ASCII for ‘!’. 
Toggling the low-order bit of 33 gives you 32, which is ASCII for a space. This causes ! to be printed if b is odd, and a blank space
to be printed if b is even.
