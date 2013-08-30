Thanks to a careless technical specialist at Neev, selection sort and quick sort just stopped working.
As a fresher, debug the program with the help of browser developer tools using breakpoints and save the day by fixing the program.

The catch - also document your steps below. 

Name : Manikanta Reddy.


--------------------

First i created the account in github.
and then I opened the link  https://github.com/emilsoman/sorting-algorithms 
and fork the repository it came to my account as my repository.
and i came to my account and copied the clone link.

open the terminal and created the folder "debugg"
I entered in to the folder in terminal and type "git clone https://github.com/manipvn/sorting-algorithms.git"
It will clone automatically in to the folder "debugg".

--------------------


I opened the index.html and i run all the sorting methods and I found selection sort and quick sort are not working perfectly

Selection Sort
==============

## Steps

1. I started the break points to know the step by step procedure.
2. I kept the BreakPoints in the line contains "for (var i = 0; i < this.a.length; i++)" and "for (var j = 0 ; j < i; j++)" to understand the 		Blocks.
3. I executed the code again based on the breakpoints.
4. refresh the page and I clicked on selection sort.
5. It stops the execution at the line contains "for (var i = 0; i < this.a.length; i++)" for further execution I press 'F5'(It will go to next 	  step) and I found 'i' value is 0 now and a.length is 50.And 'i' will increment for every loop.
6. Then again it stops the exeecution in the line contains "for (var j = 0 ; j < i; j++)" for further execution I press 'F5'.It is  verifying   the array from zero to the value 'i'. But it should verify from 'i+1' to array.length. So make changes as this.
		
		Previous One:for (var j = 0 ; j < i; j++)
		Changed One: for(var j=i+1; j< this.a.length;j++)
7.And also after the completion of the for loop which contains variable j . It will give the maximum value by j (as index) but in the cloned code maximum value is giving the 'i'. The i value is verified by the value from j with the range of["i+1" to "array.length"].
	previous code tells that from zero to 'i'. It wont give the maximum value.
8. Totally we modified three places.
	Variable 'j' must starts with i+1.//Becasuse j must verify from i+1 to length of the array.
	In the Same for loop maximum value given is i. But maximum value is array.length.
	and the third one is: maximum value is given by 'j' but in the previous code tells that maximum value is i.
9. After the modification of all then I executed again It shown the Perfect sorting order.

QuickSort
=========

## Steps

1.  Quick sort will works based on the pivot element.
2.  we first divide in to parts and then sort. Mid point is given by the function part(p,r).
3.  Here in this code pivot element is first element.
4.  Now I started with breakpoints to understand the code.
5.  I kept a break points in the line contains "function(p,r)".Here in this function the array is going to divide in to parts. (this.part(p,r)).
6.  part(p,r) function will divide the array in to small parts. Mid point is given by the function part(p,r).
7.  And I kept the break point inside the function "part" at while(true).
8.  Here pivot element is first element of the array.
9.  And I kept another break points inside while loop to verify the values of variables.
10. At this process pivot value of the array is validating (or) comparing with ending value of the array.
11. But in the "Scope variables" Column it is showing the "undefined" int he last element. at this stage the value r is giving "50". That means In the array contains 50 elements. Starting form zero and ending with 49. But the 50th index value is accessing.
12  At this stage modified the j value is r-1.
		Previous j=r;
		After Changed j=r-1;
	
	Actually in the code starting value is given by variable "p". This value is Stored in i.
       ending valus is given by variable "r"(but we are recieving the length of the array but not the index of last element of the array.). This valus will be stored in j.

13.    And also inside the condition

		if(i<j)
        	{
            		this.a.swapVerbose(i,j);
			i++;
			j--;
         	}
		in the above sample code at first time completion of swapping it will increment the i value and decrement the j value.
		here through 'i' and 'j' some elements are swapping again that is no need. I commented the both statements and executed.
14. Then again I started the execution from starting I had done almost but some values which are less is not coming front. They are in center.
15. I verified the qsort function
		there after getting the mid value as 'q'.
		Here they are dividing the array in to parts. like this
				from 'p' to 'q' as one part.
				from 'q' to 'r' as one part. 
		Here in these above two statements. 'q' is accessing two times that is the reason some elements are validating again and swapping again. For this purpose I modified like this.

				from 'p' to 'q' as one part.
				from 'q+1' to 'r' as one part.
16. I started the execution again. Now I got the perfect output for the quick sort.
