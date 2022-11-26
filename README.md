#include<stdio.h>
int setA[20];
int setB[20];
int createset(int [],int,int);
int main()
{   int n1,n2,i=1,k=1,t,value;
    printf("enter no of elements for setA:\n");
    scanf("%d",&n1);
    printf("enter no.of elements for setB:\n");
    scanf("%d",&n2);
    printf("enter first element for SetA\n");
    scanf("%d",&setA[0]);
    while(i<n1)
    {   printf("enter element:");
        scanf("%d",&value);
        t=createset(setA,value,i);
        if(t==0)
        {
            printf("duplicate elements are rejected in set\n");
        }
        else if(t==1)
        {
             setA[i++]=value;
             
        }


    }
    printf("Enter first element for setB\n");
    scanf("%d",&setB[0]);
    while(k<n2)
    {   printf("enter element:");
        scanf("%d",&value);
        t=createset(setB,value,k);
        if(t==0)
        {
            printf("duplicate elements are rejected in set\n");
        }
        else if(t==1)
        {
             setB[k++]=value;
             
        }


    }
    printf("SETA\n");
    for(i=0;i<n1;i++)
      printf("%d\n",setA[i]);
    printf("SETB\n");
    for(i=0;i<n2;i++)
      printf("%d\n",setB[i]);
    return 0;
}
int createset(int set[],int n,int i)
{
  int j,t=1;
  for(j=0;j<i;j++)
  { 
    if(set[j]==n)
    {  t=0;
      break;
    }
  }
  return (t);
}

    
