# **Calculate the value of nCr efficiently:**

## `nCr means in how many ways I can choose r different items from n items`
\
let's see an example:
    
    if n==4 && r==2, we can choose the following ways:

    {1,2},{1,3},{1,4},{2,3},{2,4},{3,4} --> 6 ways

    so nCr=6

> general formula of nCr = n ! / ( ( n - r ) ! * r ! )

if we consider `n==7`  &&  `n==5`, then we can say, 

`nCr = 7! / ( (7-5)! * 5! ) = 7.6.5.4.3.2! / (2! * 5!) = 7.6.5.4.3 / 5!`

so we can say,

> nCr = n*(n-1)*(n-2).....(n-r+1) / ( r*(r-1)*(r-2)*......3.2.1 )

we will use this formula to calculate nCr effeciently



now we consider `p=n*(n-1)*(n-2).....(n-r+1) && k=r(r-1)(r-2).....3.2.1`
so the our nCr should be `p/k`

at first we know that if r==0 than our nCr = n!/ ( (n-0)! * 0! ) = 1

else

    we can replace r with min (r, n-r) as nCr = nC(n-r)
    so we can work with the smaller value

    we will consider p=1, k=1

    then we will run a loop while r>0
    in the loop we will do p*=n, k*=r

    then we will store the gcd of p & k in M
    and do p/=M and k/=M, to make the whole 
    number smaller because p/k=(p/m)/(k/m)

    then we will do n--, r--

    at last we will return the value of p as value of k will be 1 by this time

    so the nCr = p
