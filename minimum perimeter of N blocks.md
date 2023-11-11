# **Minimum perimeter of N blocks (square):**

> ### at first let's see an example of n=4:  
>> ###	we can arrange 4 blocks in the following ways:

			[][][][]      perimeter=10

			  [][][]      perimeter=10 
			      []
			
			    [][]	  perimeter=8
			    [][]

> ### so we can say if n blocks can make a square then
> ### we get minimum perimeter  

---
---
---
---
> ## so if `(float)sqrt(N) == (sqrt(N))` then it's perfect square  
> ## Then the perimeter will be `sqrt(N)*4`

---
---
---
---

> ## if the condition is not satisfied:
>> then we will find a square that can be made by less then N blocks but with maximum blocks
>
>> to do that we can calculate `(sqrt(N))`  
> for that the perimeter will be `(sqrt(N))*4`
>
>> and for the other blocks we will check how  
 many rows of `int(sqrt(N))` blocks can be made
>
>> ##	`rows =(ceil)((n-sqrt(N)*sqrt(N))/sqrt(N))`
>
>> we will add the `row*2` with the previous perimeter


		[][][]		[][][]
		[][][]		[][][]		12
		[][][]		[][][]
		[][][]							perimeter=12+2=14
		[]		[][][]
				[]		2

* Relatated Problem:  
[problem 01](https://codeforces.com/contest/859/problem/B)

