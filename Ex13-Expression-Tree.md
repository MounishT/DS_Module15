# Ex13 Fill the First 10 Elements of an Array with a Constant using Arrays.fill()
## AIM:
To write a Java program that fills the first 10 elements of an array with a constant value using the Arrays.fill() method.
## Algorithm
1. Start the program.
2. Declare an integer array with a fixed size.
3. Use Arrays.fill() to fill the first 10 positions of the array with a constant value .
4. Display all elements of the array.
5. Stop the program.

## Program:
```
/*
Program to FILL the first 10 elements of an array with a constant value using the Arrays.fill() method.
Developed by:T MOUNISH
RegisterNumber:  212223240098
*/
import java.util.Arrays;

public class ArraysFillExample {
    public static void main(String[] args) {

        // Creating an array of size 15
        int[] arr = new int[15];

        // Filling first 10 elements with constant value 5
        Arrays.fill(arr, 0, 10, 5);

        // Displaying array elements
        System.out.println("Array elements after filling:");
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");
        }
    }
}
```

## Output:

<img width="709" height="322" alt="image" src="https://github.com/user-attachments/assets/c8aef106-1af1-4ff3-8670-95123833a55a" />


## Result:
The program successfully fills the first 10 elements of the array with the constant value 5 using the Arrays.fill() method.
