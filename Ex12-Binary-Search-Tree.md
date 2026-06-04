# Ex12 Add Elements from an Array into a TreeSet
## AIM:
To write a Java program that adds elements from an array into a TreeSet and displays the elements in sorted order.
## Algorithm
1. Start the program.
2. Create an array containing integer elements.
3. Create a TreeSet object.
4. Add all elements of the array to the TreeSet using a loop or Collections method.
5. Display the elements of the TreeSet.
6. Stop the program.

## Program:
```
/*
Program that adds elements from an array into a TreeSet and displays the elements in sorted order.
Developed by:T MOUNISH
RegisterNumber:  212223240098
*/
import java.util.*;

public class ArrayToTreeSet
 {
    public static void main(String[] args)
{

        int[] arr = {40, 10, 50, 30, 20};
        TreeSet<Integer> set = new TreeSet<Integer>();
        for (int num : arr) {
            set.add(num);
        }
        System.out.println("Elements in TreeSet (Sorted Order): " + set);
    }
}

```

## Output:

<img width="798" height="580" alt="image" src="https://github.com/user-attachments/assets/e3164f22-e559-4c04-9009-91292e909907" />


## Result:
The program successfully adds elements from an array into a TreeSet.
