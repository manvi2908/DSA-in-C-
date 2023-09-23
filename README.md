# DSA-in-C-

#BINARY SEARCH

#include<iostream>
using namespace std;
int binarySearch(int arr[], int key, int n){
	int l=0;
	int h=n-1;
	int mid=(l+(h-l))/2;
	while(l<=h)
	{
		if(key==arr[mid]){
		   return mid;}
		if(key>arr[mid]){
		   l=mid+1;}
		else{
		   h=mid-1;}
		   
		mid=(l+(h-l))/2;       
  	}
  	return -1;
}
int main()
{
   int evenarray[6]={20, 34, 56, 68, 78, 90};
   int oddarray[6]={23, 37, 59, 61, 73, 95};
   int index=binarySearch(evenarray, 78, 6);
   cout<<"Index of 78 is: "<<index<<endl;
   return 0;		
}
