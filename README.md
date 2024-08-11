Certainly! Here's a GitHub README.md format for your C++ cheat sheet. You can copy and paste this into your GitHub repository's README.md file.

```markdown
# C++ Cheat Sheet

## C++ Basics

### Headers & Namespaces
```cpp
#include <iostream>
#include <vector>
#include <algorithm> // for algorithms like sort
#include <cmath> // for math functions like sqrt
using namespace std;
```

### Main Function
```cpp
int main() {
    // Your code here
    return 0;
}
```

## Data Types

### Primitive Types
```cpp
int a = 10;
float b = 10.5;
double c = 20.123456;
char d = 'A';
bool e = true;
```

### Type Modifiers
```cpp
unsigned int a;
long long int b;
```

## Control Structures

### Conditionals
```cpp
if (condition) {
    // code
} else if (another_condition) {
    // code
} else {
    // code
}
```

### Loops
```cpp
// For loop
for (int i = 0; i < n; ++i) {
    // code
}

// While loop
int i = 0;
while (i < n) {
    // code
    ++i;
}

// Do-while loop
int i = 0;
do {
    // code
    ++i;
} while (i < n);
```

## Functions

### Definition
```cpp
int add(int a, int b) {
    return a + b;
}

void printMessage() {
    cout << "Hello, World!" << endl;
}
```

### Overloading
```cpp
int add(int a, int b) {
    return a + b;
}

double add(double a, double b) {
    return a + b;
}
```

## Arrays & Strings

### Array Initialization
```cpp
int arr[5] = {1, 2, 3, 4, 5};
vector<int> vec = {1, 2, 3, 4, 5};
```

### String Manipulation
```cpp
string str = "Hello";
cout << str.length(); // Length of the string
cout << str.substr(1, 3); // Substring from index 1 of length 3
```

## Standard Template Library (STL)

### Vectors
```cpp
vector<int> vec;
vec.push_back(10);
vec.pop_back();
```

### Maps
```cpp
map<string, int> m;
m["key"] = 10;
int value = m["key"];
```

### Sets
```cpp
set<int> s;
s.insert(10);
s.erase(10);
```

### Algorithms
```cpp
sort(vec.begin(), vec.end()); // Sort vector
reverse(vec.begin(), vec.end()); // Reverse vector
```

## Input/Output

### Reading Input
```cpp
int x;
cin >> x;
```

### Writing Output
```cpp
cout << "Value: " << x << endl;
```

## Pointers & References

### Pointer Basics
```cpp
int a = 10;
int* p = &a;
cout << *p; // Dereferencing pointer
```

### Reference Basics
```cpp
int a = 10;
int& ref = a;
ref = 20; // a is now 20
```

## Object-Oriented Programming (OOP)

### Class Definition
```cpp
class MyClass {
public:
    int data;
    void display() {
        cout << data << endl;
    }
};

MyClass obj;
obj.data = 10;
obj.display();
```

### Inheritance
```cpp
class Base {
public:
    void baseFunction() {
        cout << "Base function" << endl;
    }
};

class Derived : public Base {
public:
    void derivedFunction() {
        cout << "Derived function" << endl;
    }
};

Derived d;
d.baseFunction();
d.derivedFunction();
```

## Common Algorithms

### Binary Search
```cpp
int binarySearch(vector<int>& arr, int target) {
    int left = 0, right = arr.size() - 1;
    while (left <= right) {
        int mid = left + (right - left) / 2;
        if (arr[mid] == target) return mid;
        else if (arr[mid] < target) left = mid + 1;
        else right = mid - 1;
    }
    return -1; // Not found
}
```

### DFS and BFS
```cpp
// DFS (Depth-First Search)
void dfs(int node, vector<bool>& visited, vector<vector<int>>& adj) {
    visited[node] = true;
    for (int neighbor : adj[node]) {
        if (!visited[neighbor]) {
            dfs(neighbor, visited, adj);
        }
    }
}

// BFS (Breadth-First Search)
void bfs(int start, vector<vector<int>>& adj) {
    vector<bool> visited(adj.size(), false);
    queue<int> q;
    visited[start] = true;
    q.push(start);
    while (!q.empty()) {
        int node = q.front();
        q.pop();
        cout << node << " ";
        for (int neighbor : adj[node]) {
            if (!visited[neighbor]) {
                visited[neighbor] = true;
                q.push(neighbor);
            }
        }
    }
}
```

## Error Handling

### Exceptions
```cpp
try {
    // Code that may throw exceptions
    throw runtime_error("An error occurred");
} catch (const exception& e) {
    cout << "Exception: " << e.what() << endl;
}
```

## Miscellaneous

### Pair
```cpp
pair<int, string> p = make_pair(1, "one");
cout << p.first << " " << p.second;
```

### Tuple
```cpp
tuple<int, string, double> t = make_tuple(1, "one", 1.1);
cout << get<0>(t) << " " << get<1>(t) << " " << get<2>(t);
```
```

