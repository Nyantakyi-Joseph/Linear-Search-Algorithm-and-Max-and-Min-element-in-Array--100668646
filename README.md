# Linear-Search-Algorithm-and-Max-and-Min-element-in-Array--10668646
#include <iostream>

using namespace std;

void fnRecMaxMin(int [], int , int, int*, int*); /****************************************************************************** *Function : main
*Input parameters:
* int argc - no of commamd line arguments
* char **argv - vector to store command line argumennts *RETURNS: 0 on success ******************************************************************************/ int main( int argc, char **argv)
{ int iaArr[500000],iNum,i; int
iMax=0,iMin=0;

cout<<"\nEnter the size of the array\n"; 
cin>>iNum; 

cout<<"\nEnter the elements of the array:\n";
for(i=0;i<iNum;i++) 

cin>>iaArr[i]; 

fnRecMaxMin(iaArr, 0, iNum-1, &iMax, &iMin);

cout<<"\nMax Element = \nMin Element = \n"<< iMax<< iMin<<endl; 

return 0;
}



void fnRecMaxMin(int a[],int low,int high, int *max, int *min)
	 { int mid,max1,max2,min1,min2;
if(high-low == 1)
{ if(a[low] > a[high])
{
*max = a[low];
*min = a[high]; } else
{
*max = a[high];
*min = a[low]; }
}
else if(low == high) {
*min = *max = a[low]; }
else if(low<high)
{ mid=(low+high)/2;
} }




/*LINEAR SEARCH ALGORITHM*?======================================//
#include <iostream>
using namespace std;



	
	
	int fnLinSearch(int [], int, int);
	
	 int main(void)
	
	{ 
	int iaArr[20],iNum,iKey; 
	int i,iPos=0;
	
	
	cout<<"\nEnter the size of the array \n";
	 cin>>iNum;
	
	cout<<"\nEnter the elements of the array:\n"; 
	for(i=0;i<iNum;i++) 
	cin>>iaArr[i];
	
	 cout<<"\n enter the key element \n"; 
	cin>>iKey;
	
	iPos=fnLinSearch(iaArr,iKey,iNum);
	
	if(iPos==-1)
	
	 cout<<"\nElement not found\n";
	
	 else 
	cout<<"\nElement found at position \n" <<iPos<<endl;
	
	
	return 0; 
	}
	
	int fnLinSearch(int A[], int k, int iN)
	{
	if( iN ==0) return -1; else if( k == A[iN-1]) return iN;
	 else
	return fnLinSearch(A,k,iN-1); }


