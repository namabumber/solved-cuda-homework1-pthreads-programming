Download Link: https://assignmentchef.com/product/solved-cuda-homework1-pthreads-programming
<br>
The purpose of this assignment is to familiarize yourself with Pthreads programming.

Suppose we toss darts randomly at a square dartboard, whose bullseye is at the origin, and whose sides are two feet in length. Suppose also that there is a circle inscribed in the square dartboard. The radius of the circle is one foot, and its area is <em>π </em>square feet. If the points that are hit by the darts are uniformly distributed (and we always hit the square), then the number of darts that hit inside the circle should approximately satisfy the equation

number in circle             <em>π</em>

=      <em>,</em>

total number of tosses       4

since the ratio of the area of the circle to the area of the square is <em>π</em>/4.

We can use this formula to estimate the value of <em>π </em>with a random number generator:

<table width="610">

 <tbody>

  <tr>

   <td width="610">number_in_circle = 0;for (toss = 0; toss &lt; number_of_tosses; toss++) {x = random double between -1 and 1; y = random double between -1 and 1;distance_squared = x*x + y*y; if (distance_squared &lt;= 1) number_in_circle++;} pi_estimate = 4*number_in_circle/((double) number_of_tosses);</td>

  </tr>

 </tbody>

</table>

This is called a “Monte Carlo” method, since it uses randomness (the dart tosses). Write a Pthreads program that uses a Monte Carlo method to estimate <em>π</em>. The main thread should read in the total number of tosses and print the estimate. You may want to use long long ints for the number of hits in the circle and the number of tosses, since both may have to be very large to get a reasonable estimate of <em>π</em>.

<ul>

 <li></li>

</ul>