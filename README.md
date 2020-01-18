# Marbles



Rohit dreams he is in a shop with an infinite amount of marbles. He is allowed to select n marbles. There are marbles of k different colors. From each color there are also infinitely many marbles. Rohit wants to have at least one marble of each color, but still there are a lot of possibilities for his selection. In his effort to make a decision he wakes up. Now he asks you how many possibilities for his selection he would have had. Assume that marbles of equal color cant be distinguished, and the order of the marbles is irrelevant.

Input

The first line of input contains a number T <= 100 that indicates the number of test cases to follow. Each test case consists of one line containing n and k, where n is the number of marbles Rohit selects and k is the number of different colors of the marbles. You can assume that 1<=k<=n<=1000000.

Output

For each test case print the number of possibilities that Rohit would have had. You can assume that this number fits into a signed 64 bit integer.

Example

Input:
2
10 10
30 7

Output:
1
475020
Logic Test Case 1

Input (stdin)
2

10 10

30 7

Expected Output

1

475020
Logic Test Case 2

Input (stdin)
0

Expected Output

0





#include<stdio.h>
int main()
{
    int t;
    scanf("%d",&t);
    while(t--)
    {
              long long int n,k,a,i;
              scanf("%lld%lld",&n,&k);
              a=1ll;
              n--;
              k--;
              if(k>n/2)
              k=n-k;
              for(i=1;i<=k;i++)
              {
                               a=a*(n)/i;
                               n--;
                               }
                               printf("%lld\n",a);
                               }
                               return 0;
                               }
