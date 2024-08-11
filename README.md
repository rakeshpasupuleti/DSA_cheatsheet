


# DSA Cheat Sheet

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


## C++ Conditional Statements

### `if` Statement
Evaluates a condition and executes a block of code if the condition is true.
```cpp
if (condition) {
    // code to execute if condition is true
}
```

### `if-else` Statement
Provides an alternative block of code to execute if the condition is false.
```cpp
if (condition) {
    // code to execute if condition is true
} else {
    // code to execute if condition is false
}
```

### `if-else if-else` Ladder
Checks multiple conditions in sequence.
```cpp
if (condition1) {
    // code to execute if condition1 is true
} else if (condition2) {
    // code to execute if condition2 is true
} else {
    // code to execute if none of the above conditions are true
}
```

### `switch` Statement
Evaluates an expression and executes code corresponding to the matching case.
```cpp
switch (expression) {
    case value1:
        // code to execute if expression == value1
        break;
    case value2:
        // code to execute if expression == value2
        break;
    default:
        // code to execute if expression doesn't match any case
}
```

### Conditional (Ternary) Operator
Shorthand for simple `if-else` statements.
```cpp
condition ? expression_if_true : expression_if_false;
```

### `goto` Statement
Jumps to a specific label in the code (generally discouraged).
```cpp
goto label;
// some code
label:
    // code to execute when jumping to the label
```

### `try-catch` Blocks
Handles exceptions to manage errors.
```cpp
try {
    // code that may throw exceptions
} catch (const exception_type& e) {
    // code to handle exceptions
}
```




## C++ Loops

### `for` Loop
Used for iterating over a range with a defined start, end, and increment.
```cpp
for (initialization; condition; update) {
    // code to execute on each iteration
}
```


### `while` Loop
Executes a block of code as long as the condition is true.
```cpp
while (condition) {
    // code to execute while condition is true
}
```



### `do-while` Loop
Executes a block of code at least once, and then repeats while the condition is true.
```cpp
do {
    // code to execute
} while (condition);
```



### Range-Based `for` Loop
Introduced in C++11, it iterates over elements of a container or range.
```cpp
for (auto element : container) {
    // code to execute for each element
}
```
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

