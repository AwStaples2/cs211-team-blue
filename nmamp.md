# Profile: Neil Mamparo

- **NetID:** nmamp
- **Major:** Computer Science
- **Favorite CS Topic:** Web Development
- **Topic I Find Challenging / Want to Learn:** Data Structures

\```

#include <stdio.h>

int nthFibonacciUtil(int n, int dp[]) {
    
    // base case
    if (n <= 1) {
        return n;
    }

    // check if the result is already computed
    if (dp[n] != -1) {
        return dp[n];
    }

    // calculate Fibonacci number, store in dp
    dp[n] = nthFibonacciUtil(n - 1, dp) 
          + nthFibonacciUtil(n - 2, dp);

    return dp[n];
}

int nthFibonacci(int n) {

    // initialize dp table with -1
    int dp[n + 1];
    for (int i = 0; i <= n; i++) dp[i] = -1;

    return nthFibonacciUtil(n, dp);
}

int main() {
    int n = 5;
    int result = nthFibonacci(n);
    printf("%d", result);
    return 0;
}

\```
