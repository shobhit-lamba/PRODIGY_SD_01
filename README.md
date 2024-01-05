#include <iostream>
#include <bits/stdc++.h>
using namespace std;

void convert(double temp, string unit)
{
    double temp1=0,temp2=0;
    string s1,s2,s3;
    s1="Celcius";
    s2="Fahrenheit";
    s3="Kelvin";
    if(unit==s1)
    {
        temp1=(temp*(9.0/5.0))+32;
        temp2=temp+273.15;
        cout<<temp1<<" "<<s2<<endl<<temp2<<" "<<s3;
    }
    if(unit==s2)
    {
        temp1=(temp-32)*(5.0/9.0);
        temp2=temp1+273.15;
        cout<<temp1<<" "<<s1<<endl<<temp2<<" "<<s3;
    }
    if(unit==s3)
    {
        temp1=temp-273.15;
        temp2=(temp-273.15)*(9.0/5.0)+32;
        cout<<temp1<<" "<<s1<<endl<<temp2<<" "<<s2;
    }
}

int main()
{
    double temp;
    string unit;
    cout<<"Input the temperature value: ";
    cin>>temp;
    cout<<"Input the measurement unit (Celcius/Fahrenheit/Kelvin): ";
    cin>>unit;
    convert(temp,unit);
    return 0;
}
