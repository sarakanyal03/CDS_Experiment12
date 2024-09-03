# Experiment 12
# AIM
To implement and study constructors and destructors
# THEORY
In C++, constructors and destructors are essential ideas for controlling an object's lifecycle. To aid with your understanding and application, below is a brief synopsis and example. <br>

The purpose of constructors is that they are unique member functions that are called automatically upon the creation of an object within a class. They serve as the object's initialization. <BR>
Categories: <BR>
* By Default Constructor: Does not accept input.
* Set parameters Constructor: Accepts parameters to set the object's initial values.
* Copy Paste Constructor: A new object is created by copying an existing object using the copy constructor. <br>

The purpose of destructors is to be special member functions that are run automatically when an object is removed intentionally or goes out of scope. They are employed to carry out tidying up duties, like resource releases.<br>
Features:
* The destructor bears the class name, with a tilde (`~`) before it.
* It does not return any value and does not accept any arguments.

# CODE & OUTPUT 
* CODE A : <BR>
```
#include<iostream> 
#include<string>
using namespace std; 
class Data {
    string name;
    int roll_no;
    char dept[50];
    char division;

    public:
    Data() {
        cout<<"Name: ";
        cin>>name;
        cout<<"Roll Number: ";
        cin>>roll_no;
        cout<<"Department: ";
        cin>>dept;
        cout<<"Division: ";
        cin>>division;
    }
    void display() {
        cout<<"\n"<<"DETAILS:"<<"\n"<<name<<"  "<<roll_no<<"  "<<dept<<"  "<<division<<"\n";
    }
};
int main() 
{
    Data d1;
    d1.display();
}
```
![CODE 12A](https://github.com/sarakanyal03/CDS_Experiment12/blob/main/12A.png)
* CODE B : <BR>
```
#include<iostream>
using namespace std;
class Num
{
    public:
    Num(int c, int d)
    {
        if(c>d)
        {
            cout<<c<<" is greater.";
        }
        else 
        {
            cout<<d<<" is greater.";
        }
    }
};
int main()
{
    Num n1(4,3);
} 
```
![CODE 12B](https://github.com/sarakanyal03/CDS_Experiment12/blob/main/12B.png)
* CODE C: <BR>
![CODE 12C](https://github.com/sarakanyal03/CDS_Experiment12/blob/main/12C.png)
```
#include<iostream>
using namespace std;
int count=0;
class destruct{
    public:
    destruct()
    {
        count++;
        cout<<"Number of objects created: "<<count<<"\n";
    }
    ~destruct()
    {
        count--;
        cout<<"Number of objects destroyed: "<<count<<"\n";
    }
};
int main()
{
    destruct aa,bb,cc;
    {
        destruct dd;
    }
    return 0;
} 
```
# CONCLUSION
Gaining experience in C++ programming requires an understanding of constructors and destructors, particularly when interacting with intricate object-oriented systems. The idea of RAII (Resource Acquisition Is Initialization), which links resource management to object lifetime to lower the possibility of resource leaks and guarantee more dependable programming, was reaffirmed by this experiment. Writing more effective and maintainable C++ applications now has a strong basis thanks to the study and actual use of these concepts.
