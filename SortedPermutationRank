/*Given a string, find the rank of the string amongst its permutations sorted lexicographically.
Assume that no characters are repeated.

Example :

Input : 'acb'
Output : 2

The order permutations with letters 'a', 'c', and 'b' : 
abc
acb
bac
bca
cab
cba
The answer might not fit in an integer, so return your answer % 1000003
*/
//Solution::
vector<int> fact(int n)
{
    int temp =1,count=1;
    vector<int>v;
    v.push_back(1);
    
    while(count<=n)
    {
        v.push_back(temp% 1000003);
        count++;
        temp = ((temp% 1000003) * (count% 1000003));
    }
    return v;
}

int Solution::findRank(string A) {
    int ans=0;
    vector<int>v('z'-'A'+1,0);//there are both uppercase and lowercase letter
    vector<int>factor = fact(A.length());
    for(int i=A.length()-1;i>=0;i--)
    {
        int temp = 0;
        for(int j=0;j<(A[i]-'A') && j<('z'-'A'+1);j++)
        {
            temp = temp + v[j];
        }
        ans = ans + ((temp% 1000003) * factor[(A.length()-i-1)])% 1000003;
        ans = ans% 1000003;
        v[A[i]-'A']++;
    }
    return (ans+1)% 1000003;
}
