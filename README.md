#include<stdio.h>
#include <stdlib.h>
#include <time.h>
void TimKiem(int a[],int n, int phantu)
{
    int j;
    for(int i = 0; i < n; i++){
      
        if(phantu == a[i]){
            
            j = i;
            break;
        }
    }
    printf("\nPhan tu da lay di la: %d",a[j]);
   printf("\nPhan tu bi lay di nam o so thu: %d",j+1);    
}
int random(int minN, int maxN){
    return minN + rand() % (maxN + 1 - minN);
}

int main()
{
   int Sum;
   int arr[10];
   int Kai;
   do
   {
        printf("Nhap vao Tong day so thoa man (tong-45) chia het cho 10: \n");
        scanf("%d",&Sum);
   } while ((Sum-45)%10!=0);
   printf("Day so can tim la: \n");
   for(int i=0; i<10; i++)
   {
       arr[i]=(Sum-45)/10 +i;
       printf("\n%d ",(Sum-45)/10 +i);
   }
  srand((int)time(0));  
    int r;
    r = random(arr[0],arr[10]);
        printf("\n%d ",r);    
   TimKiem(arr,10,r);
   return 0;
}
