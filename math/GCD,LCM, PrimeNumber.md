### 최대공약수 GCD

##### Naive Approach
> 최대공약수를 구하는 가장 쉬운 방법은 2부터 min(A,B)까지 모든 정수로 나누어본다.

```cpp

	int g = 1;
	for(int i = 2; i<=min(a,b); i++){
		if(a % i == 0 && b % i == 0) {
			g =i;	
		}
	}

```

##### Euclidean Algorithm
>a를 b로 나눈 나머지를 r이라고 했을때, GCD(a,b) = GCD(b,r) -> r이 0일때 b가 gcd (재귀함수로 표현) -> 아주빠르고 naive approach보다 훨씬 효과적.


```cpp
	int gcd(int a, int b) {
		if(b ==0){
			return a;
		}
		else{
			return gcd(b, a%b);
		}
	}
```


### 소수 Prime Number
> 소수와 관련된 알고리즘 :
> 	1. 어떤수 N이 소수인지 아닌지 판별법
> 	2. N보다 작거나 같은 모든 자연수 중 소수를 찾아내는법


##### 1 . 어떤수 N이 소수인지 아닌지 ?
- Naive approach
```cpp
	bool prime(int n) {
		if(n<2){
			return false;
		}

		for(int i=2; i<n-1; i++){
			if(n %i ==0){
				return false;
			}
		
		}
		return true;

	}

```

- Algorithm O(rootN)
```cpp
bool prime(int n) {
    if(n<2) {
        return false;
    }

    for(int i =2; i*i <= n; i++) {
        if(n % i == 0){
            return false;
        }
    }
    return true;
}


```
explanation : 
> N이 소수가 되기위해선 ,2보다 크거나 같고, 루트N보다 작거나 같은 자연수로 나누어 떨어지면 안된다 :
>  이유 : N이 소수가 아니라면 N = a x b로 나타낼수있다.


##### 2 . 어떤수 N이 소수인지 아닌지 ?
   - Naive approach :
   > 위의 root N알고리즘을 활용해서 loop.


  - Sieve of Eratostheses
  > 1. 2부터 N까지 모든 수를 써놓는다.
  > 2. 아직 지워지지않은 수 중에서 가장 작은수를 찾는다
  > 3. 그 소는 소수이다.
  > 4. 이제 그 수의 배수를 모두 지운다.

```cpp

int prime[100];
int pn = 0;

bool check[101];
int n = 100;
for(int i = 2; i<=n; i++) {
    if(check[i]==false){
        prime[pn++] = i;
        for(int j = i + i; j <= n; j+=i) {
            check[j] = true;  }
}
        }
    }
}
```

---
