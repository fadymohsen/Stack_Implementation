### By Fady Mohsen

*This main file includes the stack implemenation*   <br>
*in the main function you can edit the trials*      <br>


```cpp
#include <iostream>
#include <string>
using namespace std;


// START CONSTANTS
const int maxSize = 100;
// END CONSTANTS






// START STACK CLASS IMPL. --- BY TEMPLATE
template <class t>
class stack{
    int top;
    t item[maxSize];

public:
    stack():top(-1){}



    // START IS FULL FUNCTION
    bool isFull(){
        return top==maxSize-1;
    }
    // END IS FULL FUNCTION

    // ---------------------------------------------------------

    // START IS EMPTY FUNCTION
    bool isEmpty(){
        return top<0;
    }
    // END IS EMPTY FUNCTION

    // ---------------------------------------------------------

    // PUSH FUNCTION
    void push(t element){
        if (isFull()) {        // Is Stack FULL !!!
            cout << "Error" << endl;    // Print Error
        }else{
            top ++;                     // Increasing size+1
            item[top] = element;        // Adding in Last Item
        }
    }
    // END PUSH FUCTION

    // ---------------------------------------------------------


    // START POP FUNCTION
    t pop (){
        if (isEmpty()){                  // Is Stack EMPTY !!!
            cout << "Error" << endl;    // Print Error
        }else{
            t ret_Item = item[top];   // Storing Last Item
            top--;                      // Decreasing Size-1
            return ret_Item;            // Printing Last Item
        }
    }
    // END POP FUNCTION

    // ---------------------------------------------------------


    // START GET TOP FUNCTION
    t get_top (){
        if (isEmpty()){                  // Is Stack EMPTY !!!
            cout << "Error" << endl;    // Print Error
        }else{
            int ret_Item = item[top];   // Storing Last Item
            return ret_Item;            // Printing Last Item
        }
    }
    // END GET TOP FUNCTION

    // ---------------------------------------------------------

    // START PRINT FUNCTION
    void print(){
        cout<<"[";                      // Start Brackets
        for (int i=top; i>=0; i--){     // Top --> 0
            cout<<item[i]<<" ";         // Printing Items
        }
        cout<<"]";                      // Closing Brackets
        cout<<endl;                     // New Line
    }
    // END PRINT FUNCTION

    // ---------------------------------------------------------







};
// END STACL CLASS IMPL.



int main() {
    stack<string> first_Trial;
    first_Trial.push("hamada");
    first_Trial.push("Seham");
    first_Trial.push("Mohsen");
    first_Trial.print();
    first_Trial.pop();
    first_Trial.print();

    return 0;
}
```
