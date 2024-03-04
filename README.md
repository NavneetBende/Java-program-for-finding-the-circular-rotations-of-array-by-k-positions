Circular rotation of an array by K position
Here in this program we’ll be learning about Java program for finding the circular rotations of array by k positions which means rotating the elements in the array where one rotation operation moves the last element of the array to the first position and shifts all remaining elements to the right. Consider the following indexes to be checked [0,1,2].

Circular rotation of array by k position in Java
Keypoints:-
In this section we will learn about basic knowledge which we need to know before coding the above Program. So we must have knowledge of what is an array? 

What is an array?
An array is a data structure, it is collection of similar data elements which is stored at contiguous memory locations in which each data element can be accessed directly by only using its index number.
 
How to declare an array?
To declare an array in C,a programmer specifies the type of the elements and the number of elements required by an array as follows − This is called a single-dimensional array. The arraySize must be an integer constant greater than zero and type can be any valid C data type. For example, to declare a 10-element array called balanceof type double, use this statement − Here balanceis a variable array which is sufficient to hold up to 10 double numbers.
 
About Java language:-
Java is class-based, object-oriented programming language and used for Internet-based applications. Java is a high-level
language.
Algorithm
Step 1- Initialize a class

Step 2- Enter number of elements of array

Step 3- Enter number of rotations of array.

Step 4- Enter number of indexes to be displayed.

Step 5- Input array elements

Step 6- run a for loop, i=0; i< elements; , i++.

step 7- then module your rotations with elements

Step 8- Enter the index of array to be displayed

step 9- print number of indexes and rotations.

 
Circular Rotations Of Array By K Positions
Code of Java program for finding the circular rotations of array by k positions
class Main {
    /*Function to left rotate arr[] of size n by d*/
    static void leftRotate(int arr[], int d, int n) {
        for (int i = 0; i < d; i++) leftRotatebyOne(arr, n);
    }
    static void leftRotatebyOne(int arr[], int n) {
        int i, temp;
        temp = arr[0];
        for (i = 0; i < n - 1; i++) arr[i] = arr[i + 1];
        arr[n - 1] = temp;
    }
    /* utility function to print an array */
    static void printArray(int arr[], int n) {
        for (int i = 0; i < n; i++) System.out.print(arr[i] + " ");
    }
    // Driver program to test above functions
    public
    static void main(String[] args) {
        // RotateArray rotate = new RotateArray();
        int arr[] = {1, 2, 3, 4, 5};
        leftRotate(arr, 2, 5);
        printArray(arr, 5);
    }
}
Output:

3 4 5 1 2 
