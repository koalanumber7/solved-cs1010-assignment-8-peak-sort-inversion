Download Link: https://assignmentchef.com/product/solved-cs1010-assignment-8-peak-sort-inversion
<br>
## Question 1: Peak——————————

Ash helped his professor, Professor Willow, to conduct atopographic survey of a piece of land.   He walked in astraight line, noting down the elevation of the land atevery centimeter. After he is done, he passed the data toProfessor Willow.  The professor asked, “what is the peakelevation of the land?”  Ash did not know the answer!  Hecould write a program to scan through the millions of datapoints he collected, but he knew that since you have takenCS1010, you can do a better job.  So, Ash asked for your help.

You first clarify the problem with Ash: “What is a peak?”To which Ash explained that _a peak is a location that isstrictly higher than the surrounding locations._   Ashexplained further the pattern in the data: the elevationalways either remains the same or increases as he walks.After he passed the peak, the elevation always eitherremains the same, or decreases.  But he cannot remember ifhe ever encountered a peak — it might be possible that theelevations data is always non-decreasing, or non-increasing,or there is a flat plateau where there are multiple highestlocations with the same elevation.  So, a peak might notexist.  But if there is a peak, it is guaranteed that thereis exactly one peak.

“Please, can you help me solve it in O(log n) time?”  Ashpleaded.  “Piece of cake!”  You said.

Write a program `peak` that reads from the standard inputthe following:

– An integer n (n &gt;= 3), followed by– n integers, each representing the elevation of a locationsurveyed by Ash

Then, prints, to the standard output, the index of thelocation of the peak if it exists, or `no peak` if a peakdoes not exist.   The first elevation has an index of 0.

An O(n) solution is trivial.  You will get 0 marks if yoursolution simply scans through the array linearly looking foran elevation that is the peak.  That is what Ash would doanyway!  To get full marks for correctness and efficiencyfor this solution, your code should run in O(log n) timewhen the input elevations are all distinct.  Your code isallowed to take longer than O(log n) if there are equalelevations in the input data, with the extreme case ofO(n) when all elevation values are the same (the land iscompletely flat).

Hint: Consider the middle element and its neighbors.  Can wetell if the peak lies on the left or the right of the middleelement?

### Sample Run“`<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="99f6f6f0eeedd9e9fca8a8a0">[email protected]</a>:~/as07-weitsang$ cat inputs/peak.1.in51 3 5 4 2<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="4f202026383b0f3f2a7e7e76">[email protected]</a>:~/as07-weitsang$ ./peak &lt; inputs/peak.1.in2<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="117e7e786665516174202028">[email protected]</a>:~/as07-weitsang$ cat inputs/peak.2.in31 2 3<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="cca3a3a5bbb88cbca9fdfdf5">[email protected]</a>:~/as07-weitsang$ ./peak &lt; inputs/peak.2.inno peak<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="650a0a0c121125150054545c">[email protected]</a>:~/as07-weitsang$ cat inputs/peak.3.in4-1 2 2 -1<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="99f6f6f0eeedd9e9fca8a8a0">[email protected]</a>:~/as07-weitsang$ ./peak &lt; inputs/peak.3.inno peak“`

## Question 2: Sort———————————

Professor Willow is teaching a huge class at the university.He finished grading a test and he passed a huge pile of testscripts to Ask.  He asked Ash to help him enter the gradesinto a spreadsheet, in increasing order of the student id.Ash said, “Sure!  The scripts are sorted, right?”  Theprofessor answered, “Almost!  The top portion of the pile issorted in increasing order.  The rest, in decreasing order.”The professor then left abruptly, leaving Ash to wonder howto deal with the test scripts.  Ash needed to sort thescripts in increasing order of the student id.  So hemessaged you to help him figure out an efficient algorithmto do this.  “No problemo!”, you said, “Can be done inO(n)!”  You said.  So you went ahead and wrote out thefollowing program to show Ash how he can solve his problemin O(n) time.

Write a program `sort` that reads, from the standard input,the following:

– An integer n (n &gt;= 1), followed by– n integers, each representing the student ids.

The student ids are unique, i.e., there is no duplicate inthe inputs.  The student ids from the inputs are arranged insuch a way that, the first k are in increasing order, theremaining n – k are in decreasing order.  k is not givenin the input, and 0 &lt;= k &lt;= n.

Then, prints, to the standard output, the student ids inincreasing order.

An O(n^2) or O(n log n) solution is trivial.  You willget 0 marks for correctness and efficiency if your solutionsimply uses one of the existing sorting algorithms to sortthe scripts.  Note also that you cannot use counting sorthere since a student id can be represented with anarbitrarily large integer (but still fit in a `long`).

Hint: Scan the input from both sides: front and back.

### Sample Run“`<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="8de2e2e4faf9cdfde8bcbcb4">[email protected]</a>:~/as07-weitsang$ cat inputs/sort.1.in51 3 5 4 2<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="ed8282849a99ad9d88dcdcd4">[email protected]</a>:~/as07-weitsang$ ./sort &lt; inputs/sort.2.in1 2 3 4 5<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="2d4242445a596d5d481c1c14">[email protected]</a>:~/as07-weitsang$ cat inputs/sort.2.in31 20 300<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="2649494f515266564317171f">[email protected]</a>:~/as07-weitsang$ ./sort &lt; inputs/sort.2.in1 20 300<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="096666607e7d49796c383830">[email protected]</a>:~/as07-weitsang$ cat inputs/sort.3.in1-100<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="86e9e9eff1f2c6f6e3b7b7bf">[email protected]</a>:~/as07-weitsang$ ./sort &lt; inputs/sort.3.in-100“`

## Question 3: Inversion ———————————–

Professor Willow called Ash in the evening.  “Mr. Ketchum, Itold you that the pile of scripts is almost sorted.  But Ido not know what it means by _almost_ actually.  Can youhelp me figured out how to quantify that?”  Ash is cluelessas well.  So he called you.  “Ah, I learned this in CS1010Assignment 3,” you boasted, “In the problem Kendall, wecounted the number of inversions.”  You then go on toexplain that an inversion is a pair of scripts that are outof order.  A perfectly sorted pile of scripts would havezero inversion, and an inversely sorted pile of scriptswould have n(n-1)/2 inversions.  “Let me help youto do this, in O(n) time!”

Write a program `inversion` that reads, from the standard input,the following:

– An integer n (n &gt;= 1), followed by– n integers, each representing the student ids.

The student ids are unique, i.e., there is no duplicate inthe inputs.  The student ids from the inputs are arranged insuch a way that, the first k are in increasing order, theremaining n – k are in decreasing order.  k is not givenin the input, and 0 &lt;= k &lt;= n.

You program should then prints, to the standard output, thenumber of inversions in the input.

You have already solved this problem in Assignment 3 inO(n^2) time, so, an O(n^2) solution would receive 0marks.  An O(n log n) solution will get 8 marks forcorrectness and efficiency at most. (Hint for O(n log n)solution: binary search).  To get full marks for correctnessand efficiency, you need to produce an O(n) solution (Hintfor O(n): sort).