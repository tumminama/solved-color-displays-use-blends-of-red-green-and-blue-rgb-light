Download Link: https://assignmentchef.com/product/solved-color-displays-use-blends-of-red-green-and-blue-rgb-light
<br>
Color displays use blends of red, green, and blue (RGB) light to create the colors you see. The digital representation of this concept is to store each red, green, and blue component as an eight-bit unsigned number. The value 255 represents the maximum displayable brightness of a single component, the color 0 represents no intensity/light, and 128 is halfway between the two extremes. Below are some triples of RGB values and what color they represent.

<table width="30%">

 <tbody>

  <tr>

   <td>0, 0, 0</td>

   <td>black</td>

  </tr>

  <tr>

   <td>255, 255, 255</td>

   <td>bright white</td>

  </tr>

  <tr>

   <td>255, 0, 0</td>

   <td>bright red</td>

  </tr>

  <tr>

   <td>0, 128, 0</td>

   <td>medium green</td>

  </tr>

  <tr>

   <td>128, 128, 0</td>

   <td>medium yellow</td>

  </tr>

 </tbody>

</table>

A digital image is a two-dimensional array of RGB values, where each RGB corresponds to an on-screen pixel.

For a better understanding, open an image using the program paint (under the accessories menu). Select the color menu, then edit colors, then define custom colors, and play around in the right-hand side of the pane where you can type in RGB component numbers to see what color they represent.

Because each component is only eight bits, the 24 bits required for RGB is typically stored in a single 32-bit word rather than separately. This is called a packed RGB format. This is what is used to drive all computer displays. The hexadecimal representation of orange (full red, half green, no blue) is 0x00FF0800.

The representation of half red, half green, half blue is 8421504, in hexadecimal it is: 0x00808080.

<em>Write two functions using only shifts and bit-wise logical operations.</em> One takes individual red, green, and blue components as input and returns a single 32-bit word in packed format. The second does the inverse, which is called unpacking. Test your code with some simple examples. First pack the red, green, and blue, and then unpack them to see that you get what you started with. Pay attention to the types of all input and return values to make sure that they use the least number of bits required. All of these should be unsigned numbers (there are no negative colors).

You will need to use shift operator. <strong>x=y&lt;&lt;4</strong> assigns <em>x</em> the result of shifting <em>y</em> to the left four bits. You will also be using bitwise &amp; (AND) and | (OR). Hint: in unpack, you will need to write code like this: r2=(rgb&gt;&gt;16) &amp;0xff; to unpack the value for red. To pack the values, you will need something like this: rgb = r&lt;&lt;16|g&lt;&lt;8|b;




#include &lt;iostream&gt;

using namespace std;










int pack (int r, int g, int b);

void unpack(int rgb, int &amp;r2, int &amp;g2, int &amp;b2);

int main()

{

int r, g, b, rgb;

r=128;

g=128;

b=128;

rgb=pack(r,g,b);

cout&lt;&lt;“Test pack”&lt;&lt;endl;

cout&lt;&lt;“r is: “&lt;&lt;r&lt;&lt;” g is “&lt;&lt;g&lt;&lt;” b is “&lt;&lt;b&lt;&lt;endl;

cout&lt;&lt;“rgb is “&lt;&lt;rgb&lt;&lt;endl;

unpack(rgb,r,g,b);

cout&lt;&lt;“

Test unpack”&lt;&lt;endl;

cout&lt;&lt;“r is: “&lt;&lt;r&lt;&lt;” g is “&lt;&lt;g&lt;&lt;” b is “&lt;&lt;b&lt;&lt;endl;

cout&lt;&lt;“rgb is “&lt;&lt;rgb;

cin.ignore();

return 0;

}

int pack (int r, int g, int b)

{




//Write function here




}

void unpack(int rgb, int &amp;r2, int &amp;g2, int &amp;b2)

{




//Write function here










}







Perform the following test cases. Write the number in packed format. Include a screenshot for each test case, and copy and paste your code below.

Example Test: 128, 128, 128 result packed value: 8421504

Test 1: 0,128, 0 result packed value: ____________________

Screenshot:

Test 2: 255, 255, 255 result packed value: ____________________

Screenshot:

Test 3: A number you choose Result packed value: ________________________

Screenshot:




Code: