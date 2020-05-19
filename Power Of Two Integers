//Given a positive integer which fits in a 32 bit signed integer, find if it can be expressed as A^P where P > 1 and A > 0. A and P both should be integers.

//Example

//Input : 4
//Output : True  
//as 2^2 = 4. 

//Solution::
int Solution::isPower(int x) {
    if(x==1||x==0) return 1;
    int p=2;
    float y=pow(x,1.0/p);
    while((int)y>1){
        if(y-(int)y==0)
         return 1;
        p++;
        y=pow(x,1.0/p);
    }
    return 0;

}
