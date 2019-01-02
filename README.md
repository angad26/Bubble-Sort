/*BUBBLE-SORT*/

#include<stdio.h>
void fun (int[],int);
int main()
{
	/*MAXIMUM 15 ELEMENTS*/
	int n,a[15],i,j,temp;
	printf("Enter the number of elements in the array\n");
	scanf("%d",&n);	/*Input of max number of elements in the array (MAX=15)*/
	printf("Enter the array\n");
	fun(a,n);
}	
void fun (int b[], int c)
{
	int i,temp,j;
	for(i=0;i<=c;i++)	/*Loop for input of value by user into the array*/
	{
		scanf("%d",&b[i]);
	}
	printf("After sorting:\n");
	/*Code for soriting*/
	for(i=0;i<c;i++)
	{
		for(j=0;j<c-i;j++)
		{
			if(b[j]>b[j+1])
			{
				temp=b[j+1];
				b[j+1]=b[j];
				b[j]=temp;
			}
		}
	}
	for(i=0;i<=c;i++)
	{
		printf("%d\n",b[i]); 	/*Printing result*/
	}
}
