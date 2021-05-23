This is the Change Background Project using Vanilla Javascript.

In app.js


1.Why the number 16777215?
We all know that the colors range from #000000(pitch black) to #ffffff(pure white).
The number of colors that exist from black to white as per rgb values are 16777216.
This can be calculated simply by using permutation&combination formula [result = m to the power of n => 16 to power of 6 => 16777216]
However our ultimate goal is to convert the number into hexadecimal format and 16777216 converts to 1000000 and 16777215 converts to ffffff. Hence we proceed with 167777215 as the highest number for hexadecimal conversion
2.Randomness
As we need some randomness in our output we are multiplying our magic number with Math.random() which returns floating number in range from inclusive of 0 to exclusive of 1
Math.random()*16777215
//->9653486.355498075
As seen the output is floating point and we need to cut down it to an integer for hex conversion and hence we use Math.floor() for that
Math.floor(Math.random()*16777215)
//->96953486
3.Hexadecimal conversion
 To convert a number to hexadecimal format string , we have a beautiful method toString() which accepts the number that tells to which format it has to convert.
As we are converting to string of hexa-decimal format and hence we pass 16 as the argument as follows
(96953486).toString(16)
//->934cee
Math.floor(Math.random()*16777215).toString(16);
//->12ef556
- All we need to now is just attach # before the string
var randomColor = '#'+Math.floor(Math.random()*16777215).toString(16);
//->#19feac



Click on the link to view : - https://somit17.github.io/JSChangeBackground/
