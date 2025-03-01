#include <iostream>
#include<math.h>
using namespace std;
bool ispossible(int arr[],int n,int m,int mid){
    int ans=0;
    for(int i=0;i<n;i++){
        if(arr[i]>mid){
            ans=ans+(arr[i]-mid);
        }
        if(ans>=m){
            return true;
        }
    }
    return false;
}
 int maxwoodheight(int arr[],int n,int m){
    int s=0;
    int INT_MIN=-pow(2,31);
    int e=INT_MIN;
    for(int i=0;i<n;i++){
        e=max(e,arr[i]);
    }
    int mid=s+(e-s)/2;
    int ans=-1;
    while(s<=e){
    if(ispossible(arr,n,m,mid)){
    ans=mid;
    s=mid+1;
    }
    else{
    e=mid-1;
    }
    mid=s+(e-s)/2;
    }
    return ans;
}
int main() {
    int n,m,arr[10];
	  cout<<"enter the number of trees"<<endl;
    cin>>n;
    // int n=5;
    cout<<"enter the required wood amount"<<endl;
    cin>>m;
    // int m=20;
    cout<<"enter the height of each tree"<<endl;
    for(int i=0;i<n;i++){
        cin>>arr[i];
    }
    // int arr[5]={4,42,40,26,46};
    cout<<maxwoodheight(arr,n,m);
}
