Alex Espinosa
Computer Science
Data Structures
Count ways to reach the nth stair using step 1,2, or 3

Example: 

#include <stdio.h>

    int countWays(int n) {

    if (n == 0) {
    
    return 1;
    }
    
    if (n < 1) {
        
    return 0; 
    }

    return countWays(n - 1) + countWays(n - 2) + countWays(n - 3);
    } 
};
 
int main() {
    int n = 4;
    printf("%d\n",countWays(n));
    return 0;
};


