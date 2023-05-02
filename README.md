Download Link: https://assignmentchef.com/product/solved-comp1410-assignment-1-factorials-in-terms-of-prime-numbers
<br>



The factorial of a number <em>N </em>(written <strong><em>N</em>!</strong>) is defined as the product of all the integers from 1 to <em>N</em>. It is often defined recursively as follows:

0!=1 (By definition) <em>N</em>!= <em>N </em>×(<em>N </em>−1)!

[NOTE: Factorial of a negative number is undefined, and is not permitted.]

Factorials grow very rapidly — 5! = 120, 10! = 3,628,800. One way of specifying such large numbers is by specifying the number of times each prime number occurs in it. Thus 825 could be specified as (0 1 2 0 1) (or, (2,0) (3,1) (5,2) (7,0) (11,1)) meaning no twos, 1 three, 2 fives, no sevens and 1 eleven. For this assignment, we will follow the notation as: 825 = (2^0)*(3^1)*(5^2)*(7^0)*(11^1)

[NOTE: Although it is not required, students are advised to try to compute N! using simple integer multiplication in order to determine the largest N for which the computer does not produce an overflow.  This optional exercise will underscore why this assignment is relevant in numeric computation.]

<strong>Your task is to: </strong>

Write a complete, well documented C program that will read in an integer number <em>N </em>(limited by 2 <u>&lt;</u> <em>N </em><u>&lt;</u>100) and write out its factorial in terms of the numbers of its prime factors, using the output notation explained above.

<strong>Requirements and Hints: </strong>

<ol>

 <li>You do not have to actually calculate the factorial of any number to solve this problem.</li>

 <li>Given the first prime number 2, your program logic will:

  <ol>

   <li>Determine how many times this prime number will occur in N!.</li>

   <li>Then the program will determine what is the next prime number, and go back to step a.</li>

   <li>Steps a. and b. will continue until all the prime numbers <u>&lt;</u> N are evaluated.</li>

  </ol></li>

 <li>For example: 4! = 2X3X4, where the prime 2 occurs three times (2X4) = (2X2X2) = (2^3), and the prime 3 occurs only one time, (3^1). So 4! = (2^3)*(3^1). Likewise, 5! = (2^3)*(3^1)*(5^1).</li>

 <li>Your program should implement at least the following 3 functions:

  <ol>

   <li><strong>find_prime_count()</strong>, that will count the number of a given prime in N!.</li>

   <li><strong>find_next_prime()</strong>, that, given a prime number, will determine the next prime number.</li>

   <li><strong>is_prime()</strong>, that will determine whether a number is a prime number or not.</li>

  </ol></li>

</ol>

<strong>Input: </strong>

You have to use input redirection technique to enter inputs from a text file.

<strong>Example: a.out &lt; input.txt </strong>

The input file will consist of a series of lines, each line containing a single integer <em>N</em>. The file will be terminated by a line consisting of a single <em>0</em>.

<strong>Output (you must follow the following format!): </strong>

Output will consist of a series of blocks of lines, one block for each line of the input. Each block will start with the number N, right justified in a field of width 3, and the characters <strong>`!’, </strong>space, <strong>`=’ </strong>and <strong>2 </strong>spaces.

This will be followed by a list of pairs of numbers in parenthesis, such as <strong>(x^y), </strong>separated by <strong>*, </strong>where <strong>x </strong>is a prime number and <strong>y </strong>is the number of times the prime number <strong>x </strong>occurs in <strong>N!</strong>. These should be right justified in variable width fields (shown below) and each line (except the last of a block, which may be shorter) should contain 9 pairs of numbers. Any lines after the first should be indented.




Follow the layout of the example shown below <strong>exactly</strong>.




<strong>Sample input file: </strong>

<strong>5 </strong>

<strong>53 </strong>

<strong>100 0 </strong>

<strong> </strong>

<strong>Sample output (you must follow the output format): </strong>

<strong>  5! = (2^3)*(3^1)*(5^1) </strong>

<strong> </strong>

<strong> 53! = (2^49)*(3^23)*(5^12)*(7^8)*(11^4)*(13^4)*(17^3)*(19^2)*(23^2) </strong>

<strong>      *(29^1)*(31^1)*(37^1)*(41^1)*(43^1)*(47^1)*(53^1) </strong>

<strong> </strong>

<strong>100! = (2^97)*(3^48)*(5^24)*(7^16)*(11^9)*(13^7)*(17^5)*(19^5)*(23^4) </strong>

<strong>      *(29^3)*(31^3)*(37^2)*(41^2)*(43^2)*(47^2)*(53^1)*(59^1)*(61^1) </strong>

<strong>      *(67^1)*(71^1)*(73^1)*(79^1)*(83^1)*(89^1)*(97^1) </strong>

<strong> </strong>

<strong>REQUIREMENTS: </strong>

<ul>

 <li>Write and document a complete C program that is capable of satisfying the requirements of this assignment problem.</li>

 <li>UNDOCUMENTED OR IMPROPERLY DOCUMENTED code will automatically lose 50% marks.</li>

 <li>PLAGIARIZED work will not be graded and receive a mark of ZERO and reported according to the Senate bylaws.</li>

 <li>The question requires use of I/O redirection. Please review the textbook for an example on using I/O redirection from flat files.</li>

 <li>TO SUBMIT: No later than the submission deadline, your submission must be received. Late submissions are not accepted and will receive a mark of ZERO.</li>

 <li>Submit your work through Blackboard as attachments, including both the source file (assign1.c) and the script file (assign1.txt) – see below how to create the script file.</li>

</ul>




To create a script file (one that logs your compilation steps and your output in a text file):

<ol>

 <li><strong>script assign1.txt </strong></li>

 <li><strong>cat assign1.c </strong></li>

 <li><strong>cat input.txt </strong></li>

 <li><strong>cc assign1.c </strong></li>

 <li><strong>out &lt; input.txt </strong></li>

 <li><strong>ls -l </strong></li>

 <li><strong>exit </strong>(DO NOT FORGET THIS STEP!!)</li>

</ol>





