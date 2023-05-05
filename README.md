Download Link: https://assignmentchef.com/product/solved-cse240-homework-11-functional-programs-in-dr-racket-scheme
<br>
Introduction

The aim of this assignment is to make sure that you understand and are familiar with the concepts covered in the lectures. By the end of the assignment, you should have

<ul>

 <li>understood the concepts of functional programming paradigm.</li>

 <li>written functional programs in Dr. Racket Scheme.</li>

 <li>understood names, forms, and procedures in functional programming paradigm.</li>

</ul>

<strong>Reading</strong>: Text Chapter 4, section 4.1, 4.2, and 4.3. Read course notes (slides). This is a complete new language, and you need to spent more time to read and to program.

<strong>Preparation</strong>: Complete the multiple choice questions in the textbook exercise section. The answer keys can be found in the course Web site. These exercises can help you prepare for your weekly quiz and the exam. You are encouraged to read the other exercise questions and make sure you understand these questions in the textbook exercise section, which can help you better understand what materials are expected to understand after the lectures and homework on each chapter.

You are expected to do the majority of the assignment outside the class meetings. Should you need assistance, or have questions about the assignment, please contact the instructor or the TA during their office hours.

You are encouraged to ask and answer questions on the course discussion board. However, <strong>do not share your answers and code </strong>in the course discussion board.

Practice Exercises (no submission required)

1. Tutorial: Getting Started with DrRacket

1.1. To complete this assignment, you will need to download and install a copy of Dr Racket (http://racket-lang.org/download/) on your local PC.

1.2 Start the program DrRacket.

1.3 Choose the “<strong>R5RS</strong>” from the language menu:

DrRacket menu: language →choose language →<strong>Other Languages – R5RS. </strong>

1.4. Enter your programs/forms in the upper window of DrRacket and click on the “run” button to execute your programs/forms, e.g., enter:

<table width="0">

 <tbody>

  <tr>

   <td width="198">


    <table width="0">

     <tbody>

      <tr>

       <td width="197">(write “hello world”) (newline)(write (+ (* 3 8) 10))(- 20 5)(write (read))</td>

      </tr>

     </tbody>

    </table></td>

   <td width="46"></td>

   <td width="690">


    <table width="0">

     <tbody>

      <tr>

       <td width="201">(display “hello world”) (newline) (display (+ (* 3 8) 10)) (- 20 5) (display (read)) ; input a number from keyboard</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>




Click on <strong>run</strong>, the following results should appear in the lower window:

hello world

34

15

<ol start="2">

 <li><strong>Use DrRacket to calculate the following expressions/forms. </strong></li>

</ol>

<ul>

 <li>(3 + (5 + (7 + (9 + (11 + 13))))).</li>

 <li>(((((3 + 5) + 7) + 9) + 11) + 13)</li>

 <li>((2+4)+(3+5)+(6+8))</li>

 <li>(2 + 4 + 6 + 8 + 10 + 12)</li>

 <li>(2 + 3 * 5 + 4 * 6 + 7)</li>

 <li>125187</li>

 <li>Input two integers: (* (read) (read))</li>

</ul>

<ol start="3">

 <li><strong>Write Scheme programs/forms to </strong></li>

</ol>

<ul>

 <li>find the second element of the list ‘(2 4 6 8 10 12). Your form should work for any list containing two or more elements.</li>

 <li>find the last element of the list ‘(2 4 6 8 10 12). Your form only needs to work for lists of six elements.</li>

 <li>merge the two lists ‘(1 2 3 4) and ‘(5 7 9) into a single list ‘(1 2 3 4 5 7 9)</li>

 <li>obtain the length of the list ‘(a b x y 10 12)</li>

 <li>check whether ‘(+ 2 4) is a symbol</li>

 <li>check whether ‘+ is a member of the list ‘(+ 3 4 6)</li>

 <li>check whether “+”, ‘(+ 3 5), “(* 4 6)” are strings</li>

 <li>check whether (* 3 5), ‘(/ 3 7), (1 2 3 4), “(+ 2 8) and “( 1 2 3)” are strings<strong> </strong></li>

</ul>

<strong>Programming Exercise (50 points) </strong>

In this assignment, you will be learning Scheme through the use of Dr. Racket. We would like to start with some basic concepts; trying to under prefix notation and the use procedure in Scheme. You will also implement nested procedures and recursive procedures. You may only use the procedures shown in the text and slides – not any of the additional library procedures in Scheme.

<table width="0">

 <tbody>

  <tr>

   <td width="556">1. Using Dr. Racket to compute the following expressions. </td>

   <td width="66">[5 points]</td>

  </tr>

  <tr>

   <td width="556">        1.1         19 * 12 + 25 – 33</td>

   <td width="66"> </td>

  </tr>

  <tr>

   <td width="556">        1.2         15 * ( 16 + 5 / 3 ) – 12 * 7</td>

   <td width="66"> </td>

  </tr>

  <tr>

   <td width="556">        1.3         121 * (( 15 – ( 4 * 3 )) + ( 19 / 4 ) ) * 14</td>

   <td width="66"> </td>

  </tr>

 </tbody>

</table>

<ul>

 <li>(22 + 33) * ( 21 + ( ( ( 15 / 6 ) + ( 3 * 4 ) ) / ( 5 – 7 ) ) )</li>

 <li>( ( ( ( ( ( 6 – 9 ) * ( 11 * 5 + 7 ) ) / 2 ) / 2 ) – 5 ) / 3 ) + ( ( ( ( 7 * 5 ) + ( 8 / 2 * 4 ) ) / 2 ) + ( 9 * 5 ) )</li>

 <li>Bind (define) each value in question 1.5 above to its’ English text and then change the</li>

</ul>

expression using the defined names.                                                                            [5 points]

For example, the expression 8 + 2 – 10 should be replaced with names eight, two, and ten, and the correct corresponding expression is (eight + two – ten), of course, in prefix notation.

<ul>

 <li>Define a procedure called “Subtract” that takes two parameters and returns the difference of them.</li>

</ul>

You can use the built-in “-” to define your Subtract procedure.                                                        [5 points]




&gt; (Subtract 120 50)

70

<ul>

 <li>Define a <strong>recursive</strong> procedure called “IntDivide” that will compute the quotient of x divided by y. You must implement IntDivide procedure by a sequence of “Subtract” procedures that you defined in question 3. You may not use the built-in division or quotient procedures in Scheme.

  <ul>

   <li>You must recursion to implement the iteration.</li>

   <li>You will need to account for negative values as well.</li>

  </ul></li>

</ul>

Hint: This will require a conditional and possibly the (abs x) procedure. You may not use the built-in division or quotient operators in this procedure definition.          [10 points]

&gt; (IntDivide 8 3)

2

&gt; (IntDivide 8 -3)

-2

<ul>

 <li>Define a procedure “ReadForIntDivide” to read the two input values for the IntDivide procedure defined in the previous. This procedure takes no parameters and will pass an input value to the</li>

</ul>

IntDivide procedure.                                                                                                                                          [5 points]

<sup>                 </sup>&gt; (ReadForIntDivide)

-25

<sup>                 </sup>4

-6

<ul>

 <li>Define a <strong>recursive</strong> procedure called “Multiply” that will compute the product of x times y. You must implement Multiply procedure by a sequence of additions, g., 5*3 should be implemented as</li>

</ul>

5+5+5 or 3+3+3+3+3..                                                                                                                                         [5 points]

<ul>

 <li>You can use the built-in + operation, but you cannot use the built-in “*”. You must recursively use addition to solve the problem.</li>

 <li>You will need to account for negative values as well.</li>

</ul>

&gt; (Multiply 8 3)

24

<ul>

 <li>Define a procedure (DiffDivide x y) that will compute the following expression:</li>

</ul>

x – (x/y)*y. For example, if x = 8 and y = 3, then,  8 – (8/3)*3 = 2

You must use Subtract, IntDivide, and Multiply defined in the previous questions. You cannot

use the built-in operations -, /, and *.                                                                                              [5 points]

&gt; (DiffDivide 8 3)

2

<ul>

 <li>Re-implement the procedure (DiffDivide x y) and call it (DiffDivideLet x y). In this procedure, you must use let-form to bind all the procedures used in the definition: Subtract, IntDivide, and Multiply.</li>

</ul>

You may name the local name whatever you’d like.

&gt; (DiffDivideLet 8 3)

2








