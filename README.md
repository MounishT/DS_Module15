# Ex11 Convert HashSet to ArrayList in Java

## AIM:
To convert a collection of distinct integers stored in a HashSet into an ArrayList and display its contents.
## Algorithm
1. Start the program.
2. Create a HashSet of integers and add elements into it.
3. Create an ArrayList by passing the HashSet as a parameter to the ArrayList constructor.
4. Display the HashSet elements and the converted ArrayList.
5. Stop the program.   


## Program:
```
/*
Program to To convert a collection of distinct integers stored in a HashSet into an ArrayList and display its contents.
Developed by:T MOUNISH
RegisterNumber:212223240098
*/

import java.util.*;

public class HashSetToArrayList {
    public static void main(String[] args) {

        // Creating a HashSet
        HashSet<Integer> numbers = new HashSet<Integer>();
        numbers.add(10);
        numbers.add(20);
        numbers.add(30);
        numbers.add(40);
        numbers.add(50);

        // Converting HashSet to ArrayList
        ArrayList<Integer> list = new ArrayList<Integer>(numbers);

        // Displaying contents
        System.out.println("HashSet elements: " + numbers);
        System.out.println("ArrayList elements: " + list);
    }
}

```

## Output:

<img width="445" height="182" alt="Screenshot 2025-11-15 212604" src="https://github.com/user-attachments/assets/83bfba7d-6b6e-4b08-9fb7-de7df7c6d33c" />


## Result:
The program successfully converts a collection of distinct integers stored in a HashSet into an ArrayList




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
RegisterNumber:212223240098
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

<img width="622" height="153" alt="image" src="https://github.com/user-attachments/assets/247e16b6-a92e-4905-8146-f8003004808f" />


## Result:
The program successfully adds elements from an array into a TreeSet.


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
RegisterNumber:212223240098
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

<img width="376" height="155" alt="image" src="https://github.com/user-attachments/assets/605faa91-1b39-4c07-97d3-18634f64bc9d" />


## Result:
The program successfully fills the first 10 elements of the array with the constant value 5 using the Arrays.fill() method.


# Ex14 Tracking the First Unique Number in a Stream using LinkedHashMap
## AIM:
To implement a program that tracks the first unique (non-repeating) number in a stream of integers using a LinkedHashMap.

## Algorithm
1. Start the program.
2. Initialize a LinkedHashMap<Integer, Integer> to store numbers and their frequency count.
3. For each number in the stream, update its count in the map (increment if it already exists).
4. Traverse the map entries to find the first element with a count of 1, which represents the first unique number.
5. Display the first unique number after processing the stream.
6. Stop the program.


## Program:
```
/*
Program to tracks the first unique (non-repeating) number in a stream of integers using a LinkedHashMap.
Developed by:T MOUNISH
RegisterNumber:212223240098
*/

import java.util.*;

public class FirstUniqueNumber {
    public static void main(String[] args) {

        int[] stream = {4, 5, 4, 5, 3, 2, 3, 6};

        LinkedHashMap<Integer, Integer> map = new LinkedHashMap<>();
        for (int num : stream) {
            map.put(num, map.getOrDefault(num, 0) + 1);

            System.out.print("Current First Unique Number: ");
            boolean found = false;

            for (Map.Entry<Integer, Integer> entry : map.entrySet()) {
                if (entry.getValue() == 1) {
                    System.out.println(entry.getKey());
                    found = true;
                    break;
                }
            }

            if (!found) {
                System.out.println("No Unique Number");
            }
        }
    }
}


```

## Output:

<img width="490" height="354" alt="image" src="https://github.com/user-attachments/assets/06ac50d8-8b5b-4e78-af96-7d1a89fb123c" />


## Result:
The program successfully tracks and returns the first unique number at any point in the integer stream using a LinkedHashMap.


# Ex15 Value Existence Check in a TreeMap
## AIM:
To write a Java program that checks whether a given value exists in a TreeMap.

## Algorithm
1. Start the program.
2. Create a TreeMap containing key–value pairs.
3. Display the TreeMap elements.
4. Use the containsValue() method to check if a specific value exists in the map.
5. Display whether the value is found or not.
6. Stop the program.


## Program:
```
/*
Program to checks whether a given value exists in a TreeMap.
Developed by:T MOUNISH
RegisterNumber:212223240098
*/

import java.util.*;

public class TreeMapValueCheck {
    public static void main(String[] args) {

        // Creating a TreeMap
        TreeMap<Integer, String> map = new TreeMap<Integer, String>();
        map.put(1, "Apple");
        map.put(2, "Banana");
        map.put(3, "Cherry");
        map.put(4, "Mango");

        // Display TreeMap
        System.out.println("TreeMap Elements: " + map);

        // Value to search
        String searchValue = "Mango";

        // Check value existence
        if (map.containsValue(searchValue)) {
            System.out.println("Value '" + searchValue + "' exists in the TreeMap.");
        } else {
            System.out.println("Value '" + searchValue + "' does NOT exist in the TreeMap.");
        }
    }
}

```

## Output:

<img width="490" height="354" alt="image" src="https://github.com/user-attachments/assets/5b854451-6a10-42b3-8d88-c5f9eaf5317a" />


## Result:
Thus, the program successfully checks whether a specified value exists in a TreeMap using the containsValue() method.
