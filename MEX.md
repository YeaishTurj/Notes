# ***MEX (Minimum EXcluded) :***
```
smallest number which isn't included in the set
i.e:
    A=[1,2,3], B=[0,1,3,4]
    MEX(A)=0, MEX(B)=2
```

```
now we notice the following sets:
let, no. of elements, n=3
we can create the following sets of n elements:
    [0,1,2] --> 3
    [1,2,3] --> 0
    [2,3,4] --> 1
    [3,4,5] --> 2
    [4,5,6] --> 3
    [6,7,8] --> 3
    .......
    .......
    so on
if we notice that:
        the MEX is always <= n
```

## * how to find MEX:  

		1. at first ignore all elements greater than n
		2. create a hashing array of n+1 size
		3. store 1 in the hash[element]
		4. iterate the hash array and print the first index containing 0, that's the MEX

## * another way to find MEX:

        use set_name.find("element") function
		
```python
    MEX=0;
    while(s.find(MEX)!=s.end()) MEX++;
    print(MEX)
```
