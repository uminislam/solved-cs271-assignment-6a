Download Link: https://assignmentchef.com/product/solved-cs271-assignment-6a
<br>
<ul>

 <li>Implement and test your own <em>ReadVal</em> and <em>WriteVal</em> procedures for <u>unsigned</u></li>

 <li>Implement macros <em>getString</em> and <em>displayString</em>. The macros may use Irvine’s <em>ReadString</em> to get input from the user, and <em>WriteString</em> to display output.

  <ul>

   <li><em>getString</em> should display a prompt, then get the user’s keyboard input into a memory location o <em>displayString</em> should the string stored in a specified memory location.</li>

   <li><em>readVal</em> should invoke the <em>getString</em> macro to get the user’s string of digits. It should then convert the digit string to numeric, while validating the user’s input.</li>

   <li><em>writeVal</em> should convert a numeric value to a string of digits, and invoke the <em>displayString</em> macro to produce the output.</li>

  </ul></li>

 <li>Write a small test program that gets 10 valid integers from the user and stores the numeric values in an array. The program then displays the integers, their sum, and their average.</li>

</ul>

<strong> </strong>

<strong>Requirements: </strong>

<ul>

 <li>User’s numeric input must be validated the hard way: Read the user’s input as a string, and convert the string to numeric form. If the user enters non-digits or the number is too large for 32-bit registers, an error message should be displayed and the number should be discarded.</li>

 <li>Conversion routines must appropriately use the <strong><u>lodsb</u></strong> and/or <strong><u>stosb</u></strong></li>

 <li>All procedure <u>parameters</u> must be passed on the system stack.</li>

 <li>Addresses of prompts, identifying strings, and other memory locations should be passed by address to the macros.</li>

 <li>Used registers must be saved and restored by the called procedures and macros.</li>

 <li>The stack must be “cleaned up” by the called procedure.</li>

 <li>The usual requirements regarding documentation, readability, user-friendliness, etc., apply. 8) Submit your text code file (.<em>asm</em>) to Canvas by the due date.</li>

</ul>




<strong> </strong>

<strong>Notes: </strong>

<ul>

 <li>For this assignment you are allowed to assume that the total sum of the numbers will fit inside a 32 bit</li>

</ul>

register.

<ul>

 <li>When displaying the average, you may round down to the nearest integer. For example if the sum of the 10 numbers is 3568 you may display the average as 356.<strong>  </strong></li>

</ul>

page 1 of 2

<strong>Example (user input in <em>italics</em>):</strong>

PROGRAMMING ASSIGNMENT 6: Designing low-level I/O procedures

Written by: Sheperd Cooper




Please provide 10 unsigned decimal integers.

Each number needs to be small enough to fit inside a 32 bit register. After you have finished inputting the raw numbers I will display a list of the integers, their sum, and their average value.




Please enter an unsigned number: <em>156</em>

Please enter an unsigned number: <em>51d6fd</em>

ERROR: You did not enter an unsigned number or your number was too big.

Please try again: <em>34</em>

Please enter an unsigned number: <em>186</em>

Please enter an unsigned number: <em>15616148561615630</em>

ERROR: You did not enter an unsigned number or your number was too big.

Please try again: <em>-145</em>

ERROR: You did not enter an unsigned number or your number was too big.

Please try again: <em>345</em>

Please enter an unsigned number: <em>5</em>

Please enter an unsigned number: <em>23</em>

Please enter an unsigned number: <em>51</em>

Please enter an unsigned number: <em>0</em>

Please enter an unsigned number: <em>56</em>

Please enter an unsigned number: <em>11</em>




You entered the following numbers:

156, 34, 186, 345, 5, 23, 51, 0, 56, 11

The sum of these numbers is: 867

The average is: 86




Thanks for playing!

<strong> </strong>

<strong>Extra Credit: </strong>

<ul>

 <li>1 point: <u>number each line of user input</u> and <u>display a running subtotal</u> of the user’s numbers.</li>

 <li>2 points: Handle <u>signed</u></li>

 <li>3 points: make your <em>ReadVal</em> and <em>WriteVal</em> procedures <u>recursive</u>.</li>

</ul>

4 points: implement procedures <em>ReadVal</em> and <em>WriteVal</em>  for <u>floating point values</u>, using the FPU