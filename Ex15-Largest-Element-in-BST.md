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

<img width="1025" height="761" alt="image" src="https://github.com/user-attachments/assets/41d0b12b-7276-4a2e-9537-114fee791378" />


## Result:
Thus, the program successfully checks whether a specified value exists in a TreeMap using the containsValue() method.
