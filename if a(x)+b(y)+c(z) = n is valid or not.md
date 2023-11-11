># if A\*w + B\*x + . . . + D\*z = n, where  w, x,...,z and n are given, is valid or not


* `we need to use loops where for all A, B to (before D)  `  
`will be increased from 0 to n/(respective coefficient, ie. w, x, ...)`  
`and check the expression given below:  `

			( ( n - A*w - B*x - ...) % z == 0 && ( n - A*w - B*x - ...) >= 0 ) is true or false

			if the condition is true then D = ( n - A*w - B*x - ...) / z

			
* for example:  
a=0, b=0, c=0; x, y, z, n are given 


```cpp
while(a<=n/y){
	b=0;
	while(b<=n/y){
		if( (n - a*x - b*y ) % z == 0 && (n - a*x - b*y ) >= 0)
			print(true), return;
		b++;
	}
	a++;
}
print(false);
```

**`Some problems:`**
			
* [example 01](https://codeforces.com/contest/681/problem/B)
* [example 02](https://codeforces.com/gym/104337/problem/M)
* [example 03](https://codeforces.com/contest/189/problem/A) --> 
[solution of ex-03](https://codeforces.com/contest/189/submission/210620910)
                          
