Download Link: https://assignmentchef.com/product/solved-cs2100-tutorial-1-c-and-number-systems
<br>
<ol>

 <li>In 2’s complement representation, “sign extension” is used when we want to represent an <em>n-bit</em> signed integer as an <em>m-bit</em> signed integer, where <em>m &gt; n</em>. We do this by copying the sign-bit of the <em>n-bit</em> signed <em>m – n</em> times to the left of the <em>n-bit</em> number to create an <em>m</em>-bit number.</li>

</ol>

So for example, we want to sign-extend 0b0110 to an 8-bit number. Here <em>n = 4</em>, <em>m = 8</em>, and thus we copy the sign but <em>m – n = 4</em> times, giving us 0b00000110.

Similarly if we want to sign-extend 0b1010 to an 8-bit number, we would get 0b11111010.

Show that IN GENERAL sign extension is value-preserving. For example, 0b00000110 = 0b0110 and 0b11111010 = 0b1010.




<ol start="2">

 <li>We generalize (<em>r</em> – 1)’s-complement (also called radix diminished complement) to include fraction as follows:</li>

</ol>

<h1>                        (<em>r</em> – 1)’s complement of <em>N</em> = <em>r<sup>n</sup></em> – <em>r</em><sup>–<em>m</em></sup> – <em>N</em></h1>

where <em>n</em> is the number of integer digits and <em>m</em> the number of fractional digits. (If there are no fractional digits, then <em>m</em> = 0 and the formula becomes <em>r<sup>n</sup></em> – 1 – <em>N </em>as given in class.)

For example, the 1’s complement of 011.01 is (2<sup>3</sup> – 2<sup>–2</sup>) – 011.01 = (1000 – 0.01) – 011.01 = 111.11 – 011.01 = 100.10.

Perform the following binary subtractions of values represented in 1’s complement representation <u>by using addition</u> instead. (Note: Recall that when dealing with complement representations, the two operands must have the same number of digits.)

Is sign extension used in your working? If so, highlight it.

Check your answers by converting the operands and answers to their actual decimal values.

<ul>

 <li>11 – 010.0101</li>

 <li>101 – 0111010.11</li>

</ul>




<ol start="3">

 <li>Convert the following numbers to fixed-point binary in 2’s complement, with 4 bits for the integer portion and 3 bits for the fraction portion:</li>

</ol>




<ul>

 <li>75</li>

 <li>-2.5</li>

 <li>876</li>

 <li>1</li>

</ul>




Using the binary representations you have just derived, convert them back into decimal. Comment on the compromise between range and accuracy of the fixed-point binary system.

<ol start="4">

 <li>[AY2010/2011 Semester 2 Term Test #1]</li>

</ol>

How would you represent the decimal value –0.078125 in the IEEE 754 singleprecision representation? Express your answer in hexadecimal. Show your working.




<ol start="5">

 <li>Given the partial C program shown below, complete the two functions: <strong>readArray(</strong>) to read data into an integer array (with at most 10 elements) and <strong>reverseArray()</strong> to reverse the array. For <strong>reverseArray()</strong>, you are to provide two versions: an iterative version and a recursive version. For the recursive version, you may write an auxiliary/driver function to call the recursive function.</li>

</ol>




<table width="597">

 <tbody>

  <tr>

   <td width="597"><strong>#include &lt;stdio.h&gt; </strong><strong>#define MAX 10 </strong><strong> int readArray(int [], int); void printArray(int [], int); void reverseArray(int [], int); </strong><strong> </strong><strong>int main(void) { </strong><strong> int array[MAX], numElements; </strong><strong>  numElements = readArray(array, MAX);  reverseArray(array, numElements);  printArray(array, numElements); </strong><strong> </strong><strong> return 0; </strong><strong>}  </strong><strong>int readArray(int arr[], int limit) { </strong><strong> </strong><strong> // … </strong><strong>printf(“Enter up to %d integers, terminating with a negative integer.
”, limit);  // … </strong><strong>}  </strong><strong>void reverseArray(int arr[], int size) {  </strong><strong> // … </strong><strong>}  void printArray(int arr[], int size) { </strong><strong> int i; </strong><strong>  for (i=0; i&lt;size; i++) { </strong><strong>  printf(“%d “, arr[i]); </strong><strong> } </strong><strong> printf(“
”); </strong><strong>} </strong></td>

  </tr>

 </tbody>

</table>







<ol start="6">

 <li>Trace the following program manually (do not run it on a computer) and write out its output. When you present your solution, draw diagrams to explain.</li>

</ol>

<table width="597">

 <tbody>

  <tr>

   <td width="597"><strong>#include &lt;stdio.h&gt; </strong><strong> </strong><strong>int main(void) { </strong><strong> int a = 3, *b, c, *d, e, *f; </strong><strong>  b = &amp;a;  *b = 5;   c = *b * 3;  d = b;  e = *b + c;  *d = c + e;   f = &amp;e;  a = *f + *b;   *f = *d – *b; </strong><strong>  printf(“a = %d, c = %d, e = %d
”, a, c, e);  printf(“*b = %d, *d = %d, *f = %d
”, *b, *d, *f); </strong><strong> </strong><strong> return 0; </strong><strong>} </strong></td>

  </tr>

 </tbody>

</table>




Remember to post on the LumiNUS forum if you have any queries.





