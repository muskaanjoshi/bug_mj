#include<stdio.h>
int main()
{  int x,r1,c1,r2,c2,r3,c3,k,i,j,arr[10][10],ar[10][10],pro[10][10]={{0}};
printf("Enter how many dimensions you want in your array :");
scanf("%d",&x);
switch(x)
{
		
	case 1: {
		    printf("Matrix multiplication not possible");
			break;
		    }
	case 2: {//2d array multiplication
			printf("Enter the no. of rows & columns for first matrix :\n");
			scanf("%d %d",&r1,&c1);
			printf("Enter the no. of rows and columns for second matrix: \n");
			scanf("%d %d",&r2,&c2);
			
			while(c1!=r2)
			{ printf("Enter proper rows and columns :\n");
			printf("Enter the no. of rows & columns for first matrix :\n");
			scanf("%d %d", &r1 , &c1 );
			printf("Enter the no. of rows and columns for second matrix: \n");
			scanf("%d %d", &r2 , &c2 );
			}
			
			printf("Enter elements for first matrix :\n");
			for(i=0;i<r1;++i)
			{ for(j=0;j<c1;++j)
				{ printf("Enter element a%d%d \t",i+1,j+1); 
				scanf("%d", &arr[i][j] );
				
				}
			}
			printf("Enter elements for second matrix :\n");
			for(i=0;i<r2;++i)
			{ for(j=0;j<c2;++j)
				{ printf("Enter element a%d%d \t",i+1,j+1); 
				scanf("%d", &ar[i][j] );
				
				}
			}
			
			for(i=0;i<r1;++i)
			{ for(j=0;j<c2;++j)
				{ for(k=0;k<c1;++k)
					{ pro[i][j]+=arr[i][k]*ar[k][j];
					}
				}
			}
			printf("Matrix Multiplication is :\n");
			for(i=0;i<r1;++i)
			{ for(j=0;j<c2;++j)
				{ printf("%d  ",pro[i][j]);
				  if(j==c2-1)
				  	printf("\n\n");
				
				}
			} }break;
	
    default :	{
	        printf("Error! Enter proper number\n");
 			printf("Enter how many dimensions you want in your array :");
			scanf("%d",&x);
			}break; 
}
return 0;}

