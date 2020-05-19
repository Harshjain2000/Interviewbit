/*You are given two positive numbers A and B. You need to find the maximum valued integer X such that:

X divides A i.e. A % X = 0
X and B are co-prime i.e. gcd(X, B) = 1
For example,

A = 30
B = 12
We return
X = 5
*/
//solution1
int Solution::cpFact(int A, int B) {
    int update = 1;
    for(int i=1;i<=sqrt(A);i++)
    {
        if((A%i == 0))
        {
            if(__gcd(i,B) == 1)
            update = max(update,i);
            
            if(__gcd(A/i,B) == 1){
            update = max(update,A/i);
            break;
            }
            
        }
    }
    return update;
 }
 // solution2   
 
 int Solution::cpFact(int A, int B) {
    int update = 1;
    while(__gcd(A,B)!=1){
        A=A/__gcd(A,B);
    }
    return A;
}
