# ranju_lab-10


#include<iostream>
using namespace std;

class function
{
    private:
    int a;
    int b,c;
    
    public:
   function()                                       //deafult constructor
   { 
       cout<<"This shows the deafult constructor."<<endl;
   }
   function(int x, int y)                          //parametrised constructor of two arguments
   {
       a=x; 
       b=y;
       cout<<"This is parametrised construction with value of a:"<<a<<" and b: "<<b<<endl;
   }
   function(function &c)                           //copy constructor
   {
       a=c.a;
       b=c.b;
       cout<<a<<" "<<b<<endl;
   }
   function(int p, int q,int r)                          // constructor  overloading 
   {
       a=p; 
       b=q;
       c=r;
       cout<<"This is constructor overloading with value of a:"<<a<<" and b:"<<b<<" and c: "<<c<<endl;
   }
   
};

int main()
{
    function C1;
    function C2(4,6);
    function C3(C2);
    function C4(5,6,8);
    return 0;
}
