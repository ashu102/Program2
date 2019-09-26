# Program2
Students have become secret admirers of SEGP. They find the course exciting and the
professors amusing. After a superb Mid Semester examination, it’s now time for the
results. The TAs have released the marks of students in the form of an array, where arr[i]
represents the marks of the ith student.
Since you are a curious kid, you want to find all the marks that are not smaller than those
on its right side in the array.

#include<stdio.h>

void main()

{
int n;

scanf("%d",&n);

int a[n],count=0;

for(int i=0;i<n;i++)

scanf("%d",&a[i]);

for(int i=0;i<n-1;i++)

{
count = n-1-i;

for(int j=i+1;j<n;j++)

{

if(a[i]>=a[j]) count=count - 1;

else break;


}
if(count == 0)

printf("%d ",a[i]);

}

printf("%d",a[n-1]);

}
