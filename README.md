# Structures in C

In C, a structure is a composite data type that groups variables of different data types under a single name. It allows you to create custom data types that can store multiple variables of different data types as members within a single memory block. A structure is defined using the struct keyword followed by the structure name, and its members are listed within curly braces {}.

A structure can be represented as follows:

![Representation of a structure](https://www.simplilearn.com/ice9/free_resources_article_thumb/Structure_in_C_1.png)

A structure can be implemented in C as follows:

```
struct Person {
    char name[50];
    int age;
    float height;
};
```

In the example above, a structure named Person is defined with three members: name, age, and height. The name member is an array of characters with a maximum size of 50, representing the name of the person. The age member is an integer representing the age of the person, and the height member is a floating-point number representing the height of the person.


## Operations supported by Structures

1. Declaration: Structures are declared using a structure definition, which specifies the data members and their types. For example:

```
struct Point {
    int x;
    int y;
};
```

2. Initialization: Structures can be initialized when they are declared or after they are declared. For example:

```
struct Point p1 = {0, 0}; // Initializing at declaration
struct Point p2; // Declaration
p2.x = 1; // Initialization after declaration
p2.y = 2;
```

3. Accessing data members: You can access the data members of a structure using the dot (.) operator. For example:

```
struct Point p1 = {3, 4};
int x = p1.x; // Accessing the x data member
int y = p1.y; // Accessing the y data member
```

4. Modifying data members: You can modify the data members of a structure using the dot (.) operator. For example:

```
struct Point p1 = {3, 4};
p1.x = 5; // Modifying the x data member
p1.y = 6; // Modifying the y data member
```

5. Comparison: You can compare structures for equality or inequality using the equality (==) and inequality (!=) operators, respectively. For example:

```struct Point p1 = {3, 4};
struct Point p2 = {3, 4};
if (p1.x == p2.x && p1.y == p2.y) {
    // p1 and p2 are equal
}
```

6. Passing structures to functions: You can pass structures as arguments to functions, either by value or by reference. By value means a copy of the structure is passed, and by reference means a pointer to the structure is passed. For example:

```
void printPoint(struct Point p) {
    printf("x: %d, y: %d\n", p.x, p.y);
}

struct Point p1 = {3, 4};
printPoint(p1); // Passing by value

void modifyPoint(struct Point* p) {
    p->x = 5;
    p->y = 6;
}

struct Point p2 = {3, 4};
modifyPoint(&p2); // Passing by reference
```

7. Array of structures: You can create arrays of structures to store multiple instances of the same type of data. For example:

```
struct Point points[3]; // Array of 3 Point structures

points[0].x = 1;
points[0].y = 2;
points[1].x = 3;
points[1].y = 4;
points[2].x = 5;
points[2].y = 6;
```


Structures can also be defined within structures to create nested or hierarchical data structures. Structures are commonly used in C for organizing and storing data in a structured manner, such as representing complex objects, data records, or configurations.

The program in this repository demonstrates the implementation of a structure in C.
