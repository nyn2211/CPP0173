#include<bits/stdc++.h>
using namespace std;

int main(){
	int t;
	cin >> t;
	while (t--){
		long long x,y,z,n;
		cin >> x>>y>>z>>n;
		long long a=(long long)__gcd(x,y);
		long long b=(long long)__gcd(y,z);
		long long ucln1=(long long)__gcd(a,b);
		long long bcnn1=a*(b/ucln1);
		long long bcnn2=x*y*z/bcnn1;
		long long k= pow(10,(n-1))/bcnn2;
		long long min=pow(10,(n-1));
		long long max=pow(10,n)-1;
		if(n==0){
			cout<<-1<<endl;
			continue;
		}
		if (min%bcnn2==0){
			cout<<(long long) (pow(10,(n-1)))<<endl;
			continue;
		}
		if ((long long) ((k+1)*bcnn2)>(long long)(max)){
			cout<<-1<<endl;
			continue;
		}
		if ( (long long)((k+1)*bcnn2)<=(long long)(max)){
		cout<<(long long)((k+1)*bcnn2)<<endl;
			continue;
		}
		
	}
	
}
