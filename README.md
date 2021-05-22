
    #include <stdio.h>

int main()
{
    int n;
    
   
   char* x[10]={"Fitbit Plus: 7980","IPods: 22349","MI Band: 999","Cult Pass: 2799","Macbook Pro:229900","Digital Camera: 11101","Alexa: 9999","SandwichToaster: 2195","Microwave Oven: 9800","Scale: 4999"};
   printf("number of employees:");
   scanf("%d",&n);
   int y[10]={7980,22349,999,2799,229900,11101,9999,2195,9800,4999};
   int z[10];
   
    printf(" Here the goodies that are selected for distribution are:");
    int a[n];
    
   for(int i=0;i<n;i++)
   {
    scanf("%d ",&a[i]);
   }
   for(int i=0;i<n;i++)
   {
       printf("%s ",x[a[i]]);
   }
   int k=0;
   for(int i=0;i<n;i++)
   {
       for(int j=i+1;j<n;j++)
       {
    
       
       if(y[a[i]]<y[a[j]])
       {
           int t;
           t=y[a[i]];
           y[a[i]]=y[a[j]];
           y[a[j]]=t;
       }
       
       
       }
       z[k]=y[a[i]];
       k++;
       
   }
   int s=z[0]-z[k-1];
   printf("And the difference between the chosen goodie with highest price and the lowest price is %d",s);
   
   
   
   
   
    return 0;
}
