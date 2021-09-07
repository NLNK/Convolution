/*Multiplication of two polynomials using convolution method*/
/*
Usage:
  $ gcc -o convolution convolution.c
  $ ./convolution
*/

#include <stdio.h>
#define N 4

/* Multiplication of two polynomials */
void convolution(int *result,int *a, int *b)
{   
    // padding of zeors
    int temp_a[2*N]={0};     
    int temp_b[2*N]={0};

    for(int i=0;i<N;i++)                 
    {   temp_a[i]=a[i];
        temp_b[i]=b[i];
    }    
    
    for(int i=0;i<(2*N);i++)
    {   
        result[i]=0;                
        for(int j=0;j<=i;j++)
        {                            
            result[i]+=temp_a[j]*temp_b[i-j];    
        }
    }   
}

void main()
{     
    int result[2*N]={0};
    int a[N] = {1, 2, 3, 4};    // Polynomial a
    int b[N] = {5, 6, 7, 8};    // Polynomial b

    convolution(result,a,b);    // Convolution of two polynomials of degree N
    
    printf("Polynomial a:\n");
    for(int i=0; i< N; i++)
            printf("%d  ",a[i]);   

    printf("\n\nPolynomial b:\n");
    for(int i=0; i< N; i++)
            printf("%d  ",b[i]);

    printf("\n\n\nConvolution of two polynomials a & b :\n");
    
    for(int i=0; i< 2*N; i++)
            printf("%d  ",result[i]);   
    printf("\n");

}
