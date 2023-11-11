# ***Kadane's algorithm:***  
## 1. subarray
## 2. maximize or minimize something (i,e sum, one, zero)

## `the main purpose of kadane's algorithm is to find the maximum subarray of some related things such as sum, ones, zeros.`


* to do that we will take two variable one is 'current' and the another is 'ans'
* then assign them 0
* then we will iterate the array and will check some things:
    1. if we take the current element of the array and for taking  
    that our ans will be decreased then we will make 'current' zero.   
    In other words if for taking the value our 'current' variable gets negetive then assign 'current' with 0
	2. Otherwise the 'current' will be increased depending on the problem
	3. then we will do ans = max ( ans , current )
	4. at last print the ans

	
* for example if we take an array `{-2, -3, 4, -1, -2, 1, 5, -3}`  
and we want to find the Largest Sum Contiguous Subarray then

    ```python
    current=0, sum=0						
    while(i<size){
        if( current + a[i] < 0 ) current=0;
        else current+=a[i];
        sum=max(sum, current)
        i+=1
    }
    print(sum)
    ```

		
### * now if we see the array:  


   
   > current=0, sum=0  


1. >		for i=0, 0 + -2 < 0 , so current = 0, sum=0  
2. >		for i=1, 0 + -3 < 0 , so current = 0, sum=0  
3. >		for i=2, 0 + 4 > 0,  so current = 4, sum=4  
4. >		for i=3, 4 + -1 > 0,  so current = 3, sum=4  
5. >		for i=4, 3 + -2 > 0,  so current = 1, sum=4  
6. >		for i=5, 1 + 1 > 0,  so current = 2, sum=4  
7. >		for i=6, 2 + 5 > 0,  so current = 7, sum=7  
8. >		for i=7, 7 + -3 > 0,  so current = 4, sum=7  
		
    >##    		sum=7

>Relatated Problem:  


>[problem-1](https://codeforces.com/contest/327/problem/A)  
[soloution](https://codeforces.com/contest/327/submission/210654236)

