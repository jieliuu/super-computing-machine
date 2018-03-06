# super-computing-machine
retreive from: http://www.cplusplus.com/forum/beginner/43868/
#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    int x;
    int card[52];
    int n;
    srand(time(0));
    
    for (int i=0; i<52; i++) {
        card[i] = i;
    }
    
    while (cin >> n) {
          for (int i=0; i<(52-1); i++) {
              int r = i + (rand() % (52-i));
              int temp = card[i]; card[i] = card[r]; card[r] = temp;
          }
          
          for (int c=0; c<n; c++) {
              cout << card[c] << " ";
              }
          cout << endl;
    }
    cin >> x;
    
    return 0;
    

