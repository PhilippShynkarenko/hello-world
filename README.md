# hello-world;
#include <bits/stdc++.h>

using namespace std;



int toBin () {
    setlocale(LC_CTYPE,"rus");
    string s;
    int c,n;
    cout<<"Enter a number: ";
    cin>>c;

    s=' ';
    while (c>0) {
         n=c%2;
        c=(c-n)/2;
        if (n==0) {
            s+='0';
        }
        if (n==1) {s+='1';
        }
    }

    reverse(s.begin(),s.end());
    std::cout<<s;

    return 0;
}

int fromBin () {
setlocale(LC_CTYPE,"rus");
cout<<"Enter a number: ";
int c;
cin >>c;
string s=to_string(c);
int len=s.length();
int n=0;

for (int i=0;i<len;i++) {
    char d=s[i];
    int g=d-'0';
    n=n*2+g;
 }
cout<<n;
return 0;
}

int main () {
    setlocale(LC_CTYPE,"rus");
    int x;
    cout<<"If you entering a number in a binary system, press 2, else press 10: ";
    cin>>x;
    if (x==10) {
        toBin();
    }
    else {
        fromBin();
    }
    return 0;
}
