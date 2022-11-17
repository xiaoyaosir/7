#include <stdio.h>
using namespace std;

int an[10] = {0,1,2,3,4,5,6,7,8,9};

int islegal()
{
    int a=an[0],b=an[1],c=an[2],d=an[3],e=an[4],f=an[5],g=an[6],h=an[7];
    if(a==0||e==0) return 0;

    int n1 = a*1000+b*100+c*10+d;
    int n2 = e*1000+f*100+g*10+b;
    int n3 = e*10000+f*1000+c*100+b*10+h;

    if((n1+n2)==n3) return n2;

    return 0;
}

int main()
{
    

    do {
        int tmp = islegal();
        if(tmp) {
            cout << tmp << endl;
            break;  
        }
    }while(next_permutation(an,an+10));

    return 0;

   
} 
