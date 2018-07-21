##This is mark down file
Special Shop
Creatnx now wants to decorate his house by flower pots. He plans to buy exactly N ones. He can only buy them from Triracle's shop. There are only two kind of flower pots available in that shop. The shop is very strange. If you buy X  flower pots of kind 1 then you must pay A*X^2  and  B*Y^2 if you buy  flower pots of kind 2. Please help Creatnx buys exactly  flower pots that minimizes money he pays.

Input Format

The first line contains a integer  T denoting the number of test cases.

Each of test case is described in a single line containing three space-separated integers N,A,B

SAMPLE INPUT 
2
5 1 2
10 2 4

SAMPLE OUTPUT 
17
134

#include<stdio.h>
int main()
{
    int T,N,A,B,cost=0;
    int k,i,j;
    scanf("%d",&T);
    for(k=1;k<=T;k++)
    {
        int min = 999;
        scanf("\n%d %d %d",&N,&A,&B);
        for(i=0,j=N;i<=N,j>=0;i++,j--)
        {
            cost = ((A*(i*i))+(B*(j*j)));
            if(cost<min)
                min = cost;
        }
        printf("\n%d",min);

    }
    return 0;

}
