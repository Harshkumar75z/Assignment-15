// 1) Write a program to print the elements of both the diagonals in a square matrix.
#include<iostream>
using namespace std;
int main(){
    int n;
    cout<<"Enter the Value of n : ";
    cin>>n;
    int a[n][n];
    for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
            cout<<"Enter Element : ";
            cin>>a[i][j];
        }
    }
    for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
            if(i==j || i+j==n-1){
            cout<<a[i][j]<<" ";
            }
            else cout<<" ";
        }cout<<endl;
    }
}


// 2) Write a program to rotate the matrix by 90 degrees anti-clockwise.
#include<iostream>
using namespace std;
int main(){
    int n;
    cout<<"Enter the Value of n : ";
    cin>>n;
    int arr[n][n];
    // Input
    for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
            cin>>arr[i][j];
        }
    }
    for(int i=0;i<n;i++){
        for(int j=i+1;j<n;j++){
            int temp = arr[i][j];
            arr[i][j]=arr[j][i];
            arr[j][i]=temp;
        }
    }
    for(int p=0;p<n;p++){
        int i=0;
        int j=n-1;
    while(i<=j){
        swap(arr[i][p],arr[j][p]);
        i++;
        j--;
    }   
    }
    for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
            cout<<arr[i][j]<<"  ";
        }cout<<endl;
    }
}


// 3) Write a program to print the matrix in wave form.
#include<iostream>
using namespace std;
int main(){
    int n;
    cout<<"Enter the Value of n : ";
    cin>>n;
    int arr[n][n];
    // Input
    for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
            cin>>arr[i][j];
        }
    }
    for(int j=0;j<n;j++){
        if(j%2==0){
        for(int i=n-1;i>=0;i--){
            cout<<arr[i][j]<<" ";       
                }cout<<endl;
            }
            else{
                for(int i=0;i<n;i++){
                    cout<<arr[i][j]<<" ";
                }cout<<endl;
            }
        }
    }

