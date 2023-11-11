# Some importent things: 

>##  1. properties of modular arithmetic:
>
>>* (a + b) % m = (a % m + b % m) % m
>>* (a - b) % m = (a % m - b % m) % m
>>* (a * b) % m = (a % m * b % m) % m 
>>* (a / b) % m = a * b<sup> -1</sup> % m = (a * x) % m, where x = b<sup> -1
>
* ## according to Fermat’s little theorem:  
    >
    >
    >x<sup> m-1</sup>  ≡ 1 (mod m)   
    > =>  x<sup> m-1</sup> % m ≡ 1  
    > => x<sup> m-2</sup> ≡ x<sup> -1
    >
    >b<sup> -1</sup> = b<sup> m-2

>>* (a / b) % m = (a * b^(m-2)) % m [then follow the >multiplication property]


>>## 2. prime numbers except 2 and 3 can be represented as 6n-1 or 6n+1