#include <bits/stdc++.h>
using namespace std;

struct A
{
    int start_index,end_index;
};
bool compare(A i1,A i2)
{
return (i1.end_index<i2.end_index);
}


int main() {

int t,n;
cin>>t;

while(t-->0)
{
  cin>>n;
  A m[n];
  
int start[n],end[n];

for(int i=0;i<n;i++)
{
    cin>>start[i]>>end[i];
    m[i].start_index=start[i];
    m[i].end_index=end[i];
    
}

sort(m,m+n,compare);

int startindex=m[0].start_index;
int endindex=m[0].end_index;
int k=0;

int bombs=1;

for(int i=1;i<n;i++)
{
    if(m[i].start_index<=endindex)
    {
        
    }
    else
    {
        bombs++;
        k=i;
        startindex=m[k].start_index;
        endindex=m[k].end_index;
        
       
        
    }
     
}
cout<<bombs<<endl;

}

return 0;

}












        
        
        
        
        
        
        
        
        
        
        
        
        
    






































