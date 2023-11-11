# Some good problems:

1. [Maximum Sum](https://codeforces.com/contest/1832/problem/B) -->
[solution](https://codeforces.com/contest/1832/submission/210839050)

2. [From Zero To Y](https://codeforces.com/problemset/problem/1488/A)

    ```solution:```
    ```cpp
        ll x,y; cin>>x>>y;
        ll k=0, cnt=0;
        while(1){
            ll diff=y-k;
            if(diff<x){
                cnt+=diff; break;
            }
            ll dig=floor(log10(diff)+1);
            while(1){
                ll temp=k;
                if(y>=k+x*binPow(10, dig)){
                    k+=x*binPow(10, dig); cnt++;
                    break;
                }
                dig--;
                if(dig<0) break;
            }
        }
        cout<<cnt;
    ```

    ![image](https://github.com/YeaishTurj/Notes/assets/119549787/04ec5d89-7510-4a05-9db4-bee34c602aa3)
